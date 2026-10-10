---
title: HtmlLoadOptions.web_request_timeout property
linktitle: web_request_timeout property
articleTitle: web_request_timeout property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.web_request_timeout property. The number of milliseconds to wait before the web request times out"
type: docs
weight: 80
url: /fr/python-net/aspose.words.loading/htmlloadoptions/web_request_timeout/
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
# Créez un nouvel objet HtmlLoadOptions et vérifiez son seuil de temporisation pour une requête web.
options = aw.loading.HtmlLoadOptions()
# Lors du chargement d'un document Html avec des ressources liées externement par une URL,
# Aspose.Words annulera les requêtes web qui échouent à récupérer les ressources dans cette limite de temps, en millisecondes.
self.assertEqual(100000, options.web_request_timeout)
# Définissez un WarningCallback qui enregistrera tous les avertissements survenant pendant le chargement.
warning_callback = self.ListDocumentWarnings()
options.warning_callback = warning_callback
# Chargez un tel document et vérifiez qu’une forme contenant des données d’image a été créée.
# Cette image liée nécessitera une requête web pour se charger, qui devra être terminée dans notre délai.
html = f'\n        <html>\n        <img src=""{image_uri}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">\n        </html>\n        '
# Définissez une limite de délai d’attente déraisonnable et essayez de charger à nouveau le document.
options.web_request_timeout = 0
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=options)
self.assertEqual(2, len(warning_callback.warnings()))
# Une requête web qui ne parvient pas à obtenir une image dans le délai produira quand même une image.
# Cependant, l’image sera le « x » rouge qui indique généralement des images manquantes.
image_shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(924, len(image_shape.image_data.image_bytes))
# Nous pouvons également configurer un rappel personnalisé pour récupérer les avertissements provenant des requêtes web expirées.
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

