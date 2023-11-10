---
title: SaveOptions.progress_callback property
linktitle: progress_callback property
articleTitle: progress_callback property
second_title: Aspose.Words for Python
description: "SaveOptions.progress_callback property. Called during saving a document and accepts data about saving progress."
type: docs
weight: 100
url: /python-net/aspose.words.saving/saveoptions/progress_callback/
---

## SaveOptions.progress_callback property

Called during saving a document and accepts data about saving progress.


```python
@property
def progress_callback(self) -> aspose.words.saving.IDocumentSavingCallback:
    ...

@progress_callback.setter
def progress_callback(self, value: aspose.words.saving.IDocumentSavingCallback):
    ...

```

### Remarks

Progress is reported when saving to [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX), [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC),
[SaveFormat.DOCM](../../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTM](../../../aspose.words/saveformat/#DOTM), [SaveFormat.DOTX](../../../aspose.words/saveformat/#DOTX),
[SaveFormat.DOC](../../../aspose.words/saveformat/#DOC), [SaveFormat.DOT](../../../aspose.words/saveformat/#DOT),
[SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../../aspose.words/saveformat/#MHTML), [SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB),
[SaveFormat.XAML_FLOW](../../../aspose.words/saveformat/#XAML_FLOW), or [SaveFormat.XAML_FLOW_PACK](../../../aspose.words/saveformat/#XAML_FLOW_PACK).





### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

