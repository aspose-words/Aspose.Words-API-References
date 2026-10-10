---
title: HtmlLoadOptions.web_request_timeout property
linktitle: web_request_timeout property
articleTitle: web_request_timeout property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.web_request_timeout property. The number of milliseconds to wait before the web request times out"
type: docs
weight: 80
url: /es/python-net/aspose.words.loading/htmlloadoptions/web_request_timeout/
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
# Cree un nuevo objeto HtmlLoadOptions y verifique su umbral de tiempo de espera para una solicitud web.
options = aw.loading.HtmlLoadOptions()
# Al cargar un documento Html con recursos vinculados externamente mediante una URL de dirección web,
# Aspose.Words abortará las solicitudes web que no logren obtener los recursos dentro de este límite de tiempo, en milisegundos.
self.assertEqual(100000, options.web_request_timeout)
# Establezca un WarningCallback que registre todas las advertencias que ocurran durante la carga.
warning_callback = self.ListDocumentWarnings()
options.warning_callback = warning_callback
# Cargue dicho documento y verifique que se haya creado una forma con datos de imagen.
# Esta imagen vinculada requerirá una solicitud web para cargarse, la cual deberá completarse dentro de nuestro límite de tiempo.
html = f'\n        <html>\n        <img src=""{image_uri}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">\n        </html>\n        '
# Establezca un límite de tiempo de espera irrazonable y vuelva a intentar cargar el documento.
options.web_request_timeout = 0
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=options)
self.assertEqual(2, len(warning_callback.warnings()))
# Una solicitud web que no obtenga una imagen dentro del límite de tiempo aún producirá una imagen.
# Sin embargo, la imagen será la 'x' roja que comúnmente indica imágenes faltantes.
image_shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(924, len(image_shape.image_data.image_bytes))
# También podemos configurar una devolución de llamada personalizada para capturar cualquier advertencia de solicitudes web que excedan el tiempo.
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

