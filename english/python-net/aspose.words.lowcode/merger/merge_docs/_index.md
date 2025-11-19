---
title: Merger.merge_docs method
linktitle: merge_docs method
articleTitle: merge_docs method
second_title: Aspose.Words for Python
description: "Merger.merge_docs method. Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document."
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/merger/merge_docs/
---

## merge_docs(input_documents, merge_format_mode) {#documentlist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge_docs(self, input_documents: List[aspose.words.Document], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_documents | List[[Document](../../../aspose.words/document/)] | The input documents. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

### Examples

Shows how to merge input documents to a single document instance.

```python
first_doc = aw.DocumentBuilder()
first_doc.font.size = 16
first_doc.font.color = aspose.pydrawing.Color.blue
first_doc.write('Hello first word!')
second_doc = aw.DocumentBuilder()
second_doc.write('Hello second word!')
merged_doc = aw.lowcode.Merger.merge_docs(input_documents=[first_doc.document, second_doc.document], merge_format_mode=aw.lowcode.MergeFormatMode.KEEP_SOURCE_LAYOUT)
self.assertEqual('Hello first word!\x0cHello second word!\x0c', merged_doc.get_text())
```

### See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

