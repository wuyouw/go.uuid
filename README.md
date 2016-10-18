<h1>UUID package for Go language</h1>

<p><a href="https://travis-ci.org/satori/go.uuid"><img src="https://camo.githubusercontent.com/078cc19fc0d8475c7f8b47cc54eb2f842038b767/68747470733a2f2f7472617669732d63692e6f72672f7361746f72692f676f2e757569642e706e673f6272616e63683d6d6173746572" alt="Build Status" data-canonical-src="https://travis-ci.org/satori/go.uuid.png?branch=master" style="max-width:100%;"></a>
<a href="https://coveralls.io/github/satori/go.uuid"><img src="https://camo.githubusercontent.com/666bfd05a8c5d534b9292f69384ae5234aa100e4/68747470733a2f2f636f766572616c6c732e696f2f7265706f732f6769746875622f7361746f72692f676f2e757569642f62616467652e7376673f6272616e63683d6d6173746572" alt="Coverage Status" data-canonical-src="https://coveralls.io/repos/github/satori/go.uuid/badge.svg?branch=master" style="max-width:100%;"></a>
<a href="http://godoc.org/github.com/satori/go.uuid"><img src="https://camo.githubusercontent.com/72c2c13d92376f4881bd64d2ab1ba05e59e5ac40/687474703a2f2f676f646f632e6f72672f6769746875622e636f6d2f7361746f72692f676f2e757569643f7374617475732e706e67" alt="GoDoc" data-canonical-src="http://godoc.org/github.com/satori/go.uuid?status.png" style="max-width:100%;"></a></p>

<p>This package provides pure Go implementation of Universally Unique Identifier (UUID). Supported both creation and parsing of UUIDs.</p>

<p>With 100% test coverage and benchmarks out of box.</p>

<p>Supported versions:</p>
<ul>
<li>Version 1, based on timestamp and MAC address (RFC 4122)</li>
<li>Version 2, based on timestamp, MAC address and POSIX UID/GID (DCE 1.1)</li>
<li>Version 3, based on MD5 hashing (RFC 4122)</li>
<li>Version 4, based on random numbers (RFC 4122)</li>
<li>Version 5, based on SHA-1 hashing (RFC 4122)</li>
</ul>

<h2>Installation</h2>

<p>Use the <code>go</code> command:</p>

<pre><code>$ go get github.com/satori/go.uuid
</code></pre>

<h2>Requirements</h2>

<p>UUID package requires Go &gt;= 1.2.</p>

<h2>Example</h2>

<div class="highlight highlight-source-go"><pre><span class="pl-k">package</span> main

<span class="pl-k">import</span> (
    <span class="pl-s"><span class="pl-pds">"</span>fmt<span class="pl-pds">"</span></span>
    <span class="pl-s"><span class="pl-pds">"</span>github.com/satori/go.uuid<span class="pl-pds">"</span></span>
)

<span class="pl-k">func</span> <span class="pl-en">main</span>() {
    <span class="pl-c">// Creating UUID Version 4</span>
    <span class="pl-smi">u1</span> <span class="pl-k">:=</span> uuid.<span class="pl-c1">NewV4</span>()
    fmt.<span class="pl-c1">Printf</span>(<span class="pl-s"><span class="pl-pds">"</span>UUIDv4: <span class="pl-c1">%s</span><span class="pl-cce">\n</span><span class="pl-pds">"</span></span>, u1)

    <span class="pl-c">// Parsing UUID from string input</span>
    <span class="pl-smi">u2</span>, <span class="pl-smi">err</span> <span class="pl-k">:=</span> uuid.<span class="pl-c1">FromString</span>(<span class="pl-s"><span class="pl-pds">"</span>6ba7b810-9dad-11d1-80b4-00c04fd430c8<span class="pl-pds">"</span></span>)
    <span class="pl-k">if</span> err != <span class="pl-c1">nil</span> {
        fmt.<span class="pl-c1">Printf</span>(<span class="pl-s"><span class="pl-pds">"</span>Something gone wrong: <span class="pl-c1">%s</span><span class="pl-pds">"</span></span>, err)
    }
    fmt.<span class="pl-c1">Printf</span>(<span class="pl-s"><span class="pl-pds">"</span>Successfully parsed: <span class="pl-c1">%s</span><span class="pl-pds">"</span></span>, u2)
}</pre></div>


<h2>Documentation</h2>

<p><a href="http://godoc.org/github.com/satori/go.uuid">Documentation</a> is hosted at GoDoc project.</p>

<h2>Links</h2>

<ul>
<li><a href="http://tools.ietf.org/html/rfc4122">RFC 4122</a></li>
<li><a href="http://pubs.opengroup.org/onlinepubs/9696989899/chap5.htm#tagcjh_08_02_01_01">DCE 1.1: Authentication and Security Services</a></li>
</ul>


<h2>Copyright</h2>

<p>Copyright (C) 2013-2016 by Maxim Bublis <a href="mailto:b@codemonkey.ru">b@codemonkey.ru</a>.</p>

<p>UUID package released under MIT License.
See <a href="https://github.com/satori/go.uuid/blob/master/LICENSE">LICENSE</a> for details.</p>
