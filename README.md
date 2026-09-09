```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│  praneeth reddy                                              │
│  systems · networks · security                               │
│                                                              │
│  integrated m.sc software systems · psg tech, coimbatore     │
│  semester 5 of 10 · state: running                           │
│  seeking internship · may–jul 2027                           │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

Every project here started the same way: something told me what it was doing,
and I wanted to see for myself. The gap between the two is usually where the
interesting part is.

---

## projects

<table>
<tr>
<td width="50%" valign="top">

**[ClassRoom Code](https://github.com/praneeth3696/ClassRoom-Code)**

<sub>*"this answer is correct"* → run it against a real engine and see</sub>

Full-stack coding-lab platform for a college department. Teachers publish worksheets, students solve them in-browser, and answers are auto-graded across C/C++/Java/Python plus SQL and MongoDB engines. Untrusted code is sandboxed through Judge0.

<sub>`React` `Node.js` `Express` `PostgreSQL` `Judge0` `OAuth`</sub>

</td>
<td width="50%" valign="top">

**[ModelAuth](https://github.com/praneeth3696/modelauth)**

<sub>*"you're getting the model you paid for"* → watch the output distribution</sub>

Detects silent LLM model substitutions by API providers using statistical change-point detection. No model weights, no logprobs, no reference data — only what comes back.

<sub>`Python` `NumPy` `SciPy` `Ollama` `Chart.js`</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

**[NetSpecter](https://github.com/praneeth3696/NetSpecter)**

<sub>*"this connection is private"* → read what is actually on the wire</sub>

Passive network auditor that catches credentials and sensitive data sent in plaintext over HTTP, FTP, and mail protocols. TCP stream reassembly, cloud API key detection, offline PCAP replay for forensics.

<sub>`Python` `Scapy` `libpcap` `Rich` `Linux`</sub>

</td>
<td width="50%" valign="top">

**[ModeOS](https://github.com/praneeth3696/modeos)**

<sub>*"I'll put it back how it was"* → capture the state before touching it</sub>

Terminal-based Linux utility that reconfigures brightness, volume, night light, and running processes from declarative YAML modes. Pluggable hardware backends, graceful process control, exact state reversion.

<sub>`Python` `psutil` `PyYAML` `Docker`</sub>

</td>
</tr>
</table>

<details>
<summary><sub><code>notes — the parts that were actually hard</code></sub></summary>

<br>

**ClassRoom Code** — grading happens in the application, not in the executor, so a verdict is identical whichever one ran the code; Judge0 is trusted only for what it alone knows, which is compile errors, timeouts and signals. It sandboxes with cgroups and namespaces, which is the reason it exists. The worksheet importer never accepts a model's claim about what a question should output — it executes the reference solution and takes whatever actually came back, and a solution that fails to run yields no test cases rather than an invented one.

**ModelAuth** — four detectors over the same probe stream: sliding-window KS, adaptive CUSUM, DAS-CUSUM, and a held-out fixed reference. On a subtle same-family substitution the windowed test collapses to roughly 14% detection power while CUSUM holds around 93%, because one accumulates evidence and the other keeps forgetting it. A separate experiment exists purely to find the point where the method stops working.

**NetSpecter** — flows are keyed by the TCP 5-tuple and reassembled across segment boundaries, because a credential can straddle an MTU. Buffers are bounded and idle flows are evicted, since a reassembler with unbounded state is a denial of service you inflict on yourself.

**ModeOS** — SIGTERM, a grace period, then SIGKILL, so anything holding unsaved state gets a chance to flush. Every hardware interaction sits behind a backend interface with a mock implementation, which is what lets it run and be tested where the hardware isn't.

</details>

---

## now

```console
$ tail -f ~/.local/state/now
classroom-code   sql + mongodb lab engines, ai worksheet importer
netspecter v2    tcp reassembly, multi-protocol detectors, tui dashboard
coursework       dbms · oop · computer networks · operating systems
reading          digital forensics & incident response
```

---

## stack

```
languages    python · c · c++ · java · javascript · bash
web          react · node.js · express
data         postgresql · mysql · mongodb
systems      linux · docker · git
network      scapy · wireshark
```

---

<div align="center">

<sub>[`ypr2257@gmail.com`](mailto:ypr2257@gmail.com) · [`linkedin`](https://www.linkedin.com/in/praneeth-reddy-yeddula-7836a1337/) · `coimbatore, tn`</sub>

</div>
