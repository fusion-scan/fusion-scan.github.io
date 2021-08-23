# fusion-scan.github.io

We collect the bugs detected by our static code analyzers, Pinpoint and Fusion, in this website.


## Add a new bug into the list

To add a new bug, create a pull request by adding one item like the following (you need to replace ${...} with text):

```
<li projname="${project name}" bugtype="${cwe id}">
    <div style="float: left; height: 150px; margin-right: 1cm;">
        <img src="${logo url}" width="150px"/>
    </div>
    <div style="width: 1000px">
        <a href="https://cwe.mitre.org/data/definitions/${cwe id}.html">CWE-${cwe id}: ${cwe description}</a> |
        <a href="${bug report link}", target="_blank">Report Link</a>
        <br><br>
        <p>${description of the bug}</p>
        <br><br>
    </div>
    <br clear=all><br>
</li>
```

An example:

```
<li projname="apache" bugtype="562">
    <div style="float: left; height: 150px; margin-right: 1cm;">
        <img src="/static/apache.png" width="150px"/>
    </div>
    <div style="width: 1000px">
        <a href="https://cwe.mitre.org/data/definitions/562.html">CWE-562: Return of Stack Address</a> |
        <a href="https://bz.apache.org/bugzilla/show_bug.cgi?id=61228", target="_blank">Report Link</a>
        <br><br>
        <p>An Invalid Reference to Stack Memory (modules/http/chunk_filters.c).</p>
        <br><br>
    </div>
    <br clear=all><br>
</li>
```

## Add a new CVE into the list

create a pull request by adding the following item, which simply includes the link of the cve and its description:

```
<li>
    <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-14739">CVE-2017–14739</a>:
    ImageMagick 7.0.7–4 mishandles failed memory allocation, which allows remote attackers to cause a denial of service.
</li>
```
