---
title: Document.view_options property
linktitle: view_options property
articleTitle: view_options property
second_title: Aspose.Words for Python
description: "Document.view_options property. Provides options to control how the document is displayed in Microsoft Word."
type: docs
weight: 500
url: /ru/python-net/aspose.words/document/view_options/
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
# Установите свойство "ZoomType" в "ZoomType.PageWidth", чтобы получить Microsoft Word
# для автоматического масштабирования документа по ширине страницы.
# Установите свойство "ZoomType" в "ZoomType.FullPage", чтобы получить Microsoft Word
# для автоматического масштабирования документа так, чтобы была видна вся первая страница.
# Установите свойство "ZoomType" в "ZoomType.TextFit", чтобы получить Microsoft Word
# для автоматического масштабирования документа по внутренним полям текста первой страницы.
doc.view_options.zoom_type = zoom_type
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.SetZoomType.doc')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

