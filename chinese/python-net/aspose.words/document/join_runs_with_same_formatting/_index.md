---
title: Document.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "Document.join_runs_with_same_formatting method. Joins runs with same formatting in all paragraphs of the document."
type: docs
weight: 670
url: /zh/python-net/aspose.words/document/join_runs_with_same_formatting/
---

## join_runs_with_same_formatting() {#default}

Joins runs with same formatting in all paragraphs of the document.


```python
def join_runs_with_same_formatting(self):
    ...
```

### Remarks

This is an optimization method. Some documents contain adjacent runs with same formatting.
Usually this occurs if a document was intensively edited manually.
You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../paragraph/) node in the document for adjacent [Run](../../run/)
nodes having identical properties. It ignores unique identifiers used to track editing sessions of run
creation and modification. First run in every joining sequence accumulates all text. Remaining
runs are deleted from the document.




### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


### Examples

Shows how to join runs in a document to reduce unneeded runs.

```python
# 打开包含相邻且格式相同的文本运行的文档，
# 这通常发生在我们在 Microsoft Word 中多次编辑同一段落时。
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# 如果这些运行中有任意数量相邻且格式相同，
# 那么文档可以被简化。
self.assertEqual(317, doc.get_child_nodes(aw.NodeType.RUN, True).count)
# 使用此方法合并这些运行，并验证将进行的运行合并次数。
self.assertEqual(121, doc.join_runs_with_same_formatting())
# 合并后，我们拥有的合并次数和运行数量
# 应该等于最初的运行数量之和。
self.assertEqual(196, doc.get_child_nodes(aw.NodeType.RUN, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

