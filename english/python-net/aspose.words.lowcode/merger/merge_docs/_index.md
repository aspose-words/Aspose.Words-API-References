---
title: Merger.merge_docs method
linktitle: merge_docs method
articleTitle: merge_docs method
second_title: Aspose.Words for Python
description: "Merger.merge_docs method. Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document."
type: docs
weight: 20
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
first_doc = DocumentBuilder()
first_doc.font.size = 16
first_doc.font.color = Color.blue
first_doc.write("Hello first word!")

second_doc = DocumentBuilder()
second_doc.write("Hello second word!")

merged_doc = Merger.merge_docs([first_doc.document, second_doc.document], MergeFormatMode.KEEP_SOURCE_LAYOUT)

self.assertEqual("Hello first word!\fHello second word!\f", merged_doc.get_text())
```

### See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

