---
title: HtmlLoadOptions.ignore_noscript_elements property
linktitle: ignore_noscript_elements property
articleTitle: ignore_noscript_elements property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.ignore_noscript_elements property. Gets or sets a value indicating whether to ignore <noscript> HTML elements"
type: docs
weight: 40
url: /python-net/aspose.words.loading/htmlloadoptions/ignore_noscript_elements/
---

## HtmlLoadOptions.ignore_noscript_elements property

Gets or sets a value indicating whether to ignore \<noscript\> HTML elements.
Default value is ``False``.



```python
@property
def ignore_noscript_elements(self) -> bool:
    ...

@ignore_noscript_elements.setter
def ignore_noscript_elements(self, value: bool):
    ...

```

### Remarks

Like MS Word, Aspose.Words does not support scripts and by default loads content of \<noscript\> elements
into the resulting document. In most browsers, however, scripts are supported and content from \<noscript\>
is not visible. Setting this property to ``True`` forces Aspose.Words to ignore all \<noscript\> elements
and helps to produce documents that look closer to what is seen in browsers.



### Examples

Shows how to ignore \<noscript\> HTML elements.

```python
html = '\n                <html>\n                  <head>\n                    <title>NOSCRIPT</title>\n                      <meta http-equiv=""Content-Type"" content=""text/html; charset=utf-8"">\n                      <script type=""text/javascript"">\n                        alert(""Hello, world!"");\n                      </script>\n                  </head>\n                <body>\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\n                </body>\n                </html>'
html_load_options = aw.loading.HtmlLoadOptions()
html_load_options.ignore_noscript_elements = ignore_noscript_elements
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=html_load_options)
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.IgnoreNoscriptElements.pdf')
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

