---
title: Paragraph.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "Paragraph.join_runs_with_same_formatting method. Joins runs with the same formatting in the paragraph."
type: docs
weight: 300
url: /python-net/aspose.words/paragraph/join_runs_with_same_formatting/
---

## join_runs_with_same_formatting() {#default}

Joins runs with the same formatting in the paragraph.


```python
def join_runs_with_same_formatting(self):
    ...
```

### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


### Examples

Shows how to simplify paragraphs by merging superfluous runs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert four runs of text into the paragraph.
builder.write("Run 1. ")
builder.write("Run 2. ")
builder.write("Run 3. ")
builder.write("Run 4. ")

# If we open this document in Microsoft Word, the paragraph will look like one seamless text body.
# However, it will consist of four separate runs with the same formatting. Fragmented paragraphs like this
# may occur when we manually edit parts of one paragraph many times in Microsoft Word.
para = builder.current_paragraph

self.assertEqual(4, para.runs.count)

# Change the style of the last run to set it apart from the first three.
para.runs[3].font.style_identifier = aw.StyleIdentifier.EMPHASIS

# We can run the "join_runs_with_same_formatting" method to optimize the document's contents
# by merging similar runs into one, reducing their overall count.
# This method also returns the number of runs that this method merged.
# These two merges occurred to combine Runs #1, #2, and #3,
# while leaving out Run #4 because it has an incompatible style.
self.assertEqual(2, para.join_runs_with_same_formatting())

# The number of runs left will equal the original count
# minus the number of run merges that the "join_runs_with_same_formatting" method carried out.
self.assertEqual(2, para.runs.count)
self.assertEqual("Run 1. Run 2. Run 3. ", para.runs[0].text)
self.assertEqual("Run 4. ", para.runs[1].text)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

