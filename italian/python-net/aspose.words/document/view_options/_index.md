---
title: Document.view_options property
linktitle: view_options property
articleTitle: view_options property
second_title: Aspose.Words for Python
description: "Document.view_options property. Provides options to control how the document is displayed in Microsoft Word."
type: docs
weight: 500
url: /it/python-net/aspose.words/document/view_options/
---

## Document.view_options property

Provides options to control how the document is displayed in Microsoft Word.


```python
@property
def view_options(self) -> aspose.words.settings.ViewOptions:
    ...

```

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
doc.view_options.view_type = aw.settings.ViewType.PAGE_LAYOUT
doc.view_options.zoom_percent = 50
self.assertEqual(aw.settings.ZoomType.CUSTOM, doc.view_options.zoom_type)
self.assertEqual(aw.settings.ZoomType.NONE, doc.view_options.zoom_type)
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.SetZoomPercentage.doc')
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Imposta la proprietà "ZoomType" su "ZoomType.PageWidth" per ottenere Microsoft Word
# per ingrandire automaticamente il documento in modo da adattarlo alla larghezza della pagina.
# Imposta la proprietà "ZoomType" su "ZoomType.FullPage" per ottenere Microsoft Word
# per ingrandire automaticamente il documento in modo da rendere visibile l'intera prima pagina.
# Imposta la proprietà "ZoomType" su "ZoomType.TextFit" per ottenere Microsoft Word
# per ingrandire automaticamente il documento in modo da adattarlo ai margini interni del testo della prima pagina.
doc.view_options.zoom_type = zoom_type
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.SetZoomType.doc')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

