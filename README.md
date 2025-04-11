<h1>TCP Proxy Server</h1>

<p>
  This project implements a <strong>TCP Proxy Server</strong> in C++ using the <code>epoll</code> mechanism and a thread pool for efficient connection handling. The proxy server listens for incoming connections on a specified local IP and port, then forwards the traffic to a specified remote IP and port.
</p>

<h2>Features</h2>
<ul>
  <li>Non-blocking I/O using <code>epoll</code></li>
  <li>Multi-threaded handling of client connections with a thread pool</li>
  <li>Simple implementation without third-party networking libraries</li>
</ul>

<h2>Technologies Used</h2>
<ul>
  <li>C++</li>
  <li>epoll</li>
  <li>threadpool</li>
  <li>pthreads</li>
</ul>

<h2>Project Structure</h2>
<ul>
  <li><code>proxy_server.cpp</code>: Main implementation of the TCP Proxy Server</li>
  <li><code>Makefile</code>: Script to compile the C++ code</li>
  <li><code>server.py</code>: Simple Python server script for testing</li>
  <li><code>client.py</code>: Simple Python client script for testing</li>
</ul>

<h2>Compilation and Execution</h2>

<h3>Requirements</h3>
<ul>
  <li>g++ compiler</li>
  <li>make</li>
  <li>Python 3</li>
</ul>

<h3>Compilation</h3>
<ol>
  <li>Compile the proxy server using make:
    <pre><code>make</code></pre>
  </li>
</ol>

<h3>Running the TCP Proxy Server</h3>
<ol>
  <li>Ensure you have compiled the <code>proxy_server</code> executable.</li>
  <li>Open a terminal and start the TCP Proxy Server:
    <pre><code>./proxy_server &lt;local_ip&gt; &lt;local_port&gt; &lt;remote_ip&gt; &lt;remote_port&gt;</code></pre>
    Example:
    <pre><code>./proxy_server 127.0.0.1 8080 127.0.0.1 9090</code></pre>
  </li>
</ol>

<h3>Running the Test Server and Client</h3>
<ol>
  <li>Open a terminal and navigate to the project directory. Start the Python test server:
    <pre><code>python3 server.py</code></pre>
  </li>
  <li>Open another terminal and navigate to the project directory. Start the Python test client:
    <pre><code>python3 client.py</code></pre>
  </li>
</ol>

<p>The client will connect to the proxy server, which in turn will forward the traffic to the test server.</p>
