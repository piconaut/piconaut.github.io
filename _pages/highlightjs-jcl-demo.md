---
layout: page
title: JCL
---
Paste JCL below! Some <a href="https://www.ibm.com/docs/en/zos/2.4.0?topic=apis-examples-jcl" target="_blank">IBM sample JCL</a> looks pretty good here.

<html>
<body>
<textarea id='intext' rows=10 cols=80 placeholder='Paste JCL here!'></textarea><br>
<button id='submitbtn'>Highlight JCL!!</button>
<pre><code id='highlightedCode' class="language-jcl">
</code></pre>

</body>
</html>
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.2.0/highlight.min.js"></script>
<script type="text/javascript" src="./jcl.min.js"></script>
<script type="text/javascript" src="./gen.js"></script>
<script type="text/javascript">
  hljs.highlightAll();
</script>
