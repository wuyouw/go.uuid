#UUID package for Go language
=

    This package provides pure Go implementation of Universally Unique Identifier (UUID). Supported both creation and parsing of UUIDs.

    With 100% test coverage and benchmarks out of box.

    Supported versions:

    * Version 1, based on timestamp and MAC address (RFC 4122)
    * Version 2, based on timestamp, MAC address and POSIX UID/GID (DCE 1.1)
    * Version 3, based on MD5 hashing (RFC 4122)
    * Version 4, based on random numbers (RFC 4122)
    * Version 5, based on SHA-1 hashing (RFC 4122)


##Installation
-
Use the `go` command:
```
$ go get github.com/satori/go.uuid
```

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
