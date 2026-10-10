---
title: HtmlLoadOptions.web_request_timeout property
linktitle: web_request_timeout property
articleTitle: web_request_timeout property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.web_request_timeout property. The number of milliseconds to wait before the web request times out"
type: docs
weight: 80
url: /sv/python-net/aspose.words.loading/htmlloadoptions/web_request_timeout/
---

## HtmlLoadOptions.web_request_timeout property

The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds
(100 seconds).


```python
@property
def web_request_timeout(self) -> int:
    ...

@web_request_timeout.setter
def web_request_timeout(self, value: int):
    ...

```

### Remarks

The number of milliseconds that Aspose.Words waits for a response, when loading external resources (images, style
sheets) linked in HTML and MHTML documents.


### Examples

Shows how to set a time limit for web requests when loading a document with external resources linked by URLs.

```python
image_uri = 'https://samplelib.com/png/sample-alpha-circle-400x300.png'
# Skapa ett nytt HtmlLoadOptions-objekt och verifiera dess tidsgräns för en webbförfrågan.
options = aw.loading.HtmlLoadOptions()
# När ett Html-dokument laddas med resurser som är externt länkade via en webbadress URL,
# kommer Aspose.Words att avbryta webbförfrågningar som misslyckas med att hämta resurserna inom denna tidsgräns, i millisekunder.
self.assertEqual(100000, options.web_request_timeout)
# Ställ in en WarningCallback som kommer att registrera alla varningar som uppstår under inläsning.
warning_callback = self.ListDocumentWarnings()
options.warning_callback = warning_callback
# Läs in ett sådant dokument och verifiera att en form med bilddata har skapats.
# Den här länkade bilden kommer att kräva en webbförfrågan för att laddas, vilket måste slutföras inom vår tidsgräns.
html = f'\n        <html>\n        <img src=""{image_uri}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">\n        </html>\n        '
# Ställ in en orimlig tidsgräns och försök läsa in dokumentet igen.
options.web_request_timeout = 0
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=options)
self.assertEqual(2, len(warning_callback.warnings()))
# En webbförfrågan som misslyckas med att hämta en bild inom tidsgränsen kommer fortfarande att producera en bild.
# Dock kommer bilden att vara det röda 'x' som vanligtvis betyder saknade bilder.
image_shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(924, len(image_shape.image_data.image_bytes))
# Vi kan också konfigurera en anpassad återuppringning för att fånga upp eventuella varningar från tidsutlöpta webbförfrågningar.
self.assertEqual(aw.loading.WarningSource.HTML, warning_callback.warnings()[0].source)
self.assertEqual(aw.loading.WarningType.DATA_LOSS, warning_callback.warnings()[0].warning_type)
self.assertEqual(f"Couldn't load a resource from '{image_uri}'.", warning_callback.warnings()[0].description)
self.assertEqual(aw.loading.WarningSource.HTML, warning_callback.warnings()[1].source)
self.assertEqual(aw.loading.WarningType.DATA_LOSS, warning_callback.warnings()[1].warning_type)
self.assertEqual('Image has been replaced with a placeholder.', warning_callback.warnings()[1].description)
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.WebRequestTimeout.docx')
```

Shows how to set a time limit for web requests when loading a document with external resources linked by URLs (ListDocumentWarnings).

```python
class ListDocumentWarnings(aw.IWarningCallback):

    def __init__(self):
        self.m_warnings = []

    def warning(self, info):
        self.m_warnings.append(info)

    def warnings(self):
        return self.m_warnings
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

