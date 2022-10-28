---
title: ignore_noscript_elements property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value indicating whether to ignore <noscript> HTML elements"
type: docs
weight: 40
url: /python-net/aspose.words.loading/htmlloadoptions/ignore_noscript_elements/
---

## HtmlLoadOptions.ignore_noscript_elements property

Gets or sets a value indicating whether to ignore \<noscript\> HTML elements.
Default value is ``False``.


Like MS Word, Aspose.Words does not support scripts and by default loads content of \<noscript\> elements
into the resulting document. In most browsers, however, scripts are supported and content from \<noscript\>
is not visible. Setting this property to ``True`` forces Aspose.Words to ignore all \<noscript\> elements
and helps to produce documents that look closer to what is seen in browsers.



### Examples

Shows how to ignore \<noscript\> HTML elements.

```python
html = """
    <html>
      <head>
        <title>NOSCRIPT</title>
          <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">
          <script type=""text/javascript"">
            alert(""Hello, world!"")
          </script>
      </head>
    <body>
      <noscript><p>Your browser does not support JavaScript!</p></noscript>
    </body>
    </html>"""

html_load_options = aw.loading.HtmlLoadOptions()
html_load_options.ignore_noscript_elements = ignore_noscript_elements

doc = aw.Document(io.BytesIO(html.encode("utf-8")), html_load_options)
doc.save(ARTIFACTS_DIR + "HtmlLoadOptions.ignore_noscript_elements.pdf")
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

