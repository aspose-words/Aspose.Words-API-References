---
title: ChmLoadOptions.original_file_name property
linktitle: original_file_name property
articleTitle: original_file_name property
second_title: Aspose.Words for Python
description: "ChmLoadOptions.original_file_name property. The name of the CHM file"
type: docs
weight: 20
url: /python-net/aspose.words.loading/chmloadoptions/original_file_name/
---

## ChmLoadOptions.original_file_name property

The name of the CHM file.
Default value is ``None``.


CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links
and normally uses [Document.original_file_name](../../../aspose.words/document/original_file_name/) to check whether the file referenced by a link
is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified
explicitly via this property, since it cannot be determined automatically.


If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take
priority over the actual name of the file stored in [Document.original_file_name](../../../aspose.words/document/original_file_name/).





### Examples

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```python
# Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
# so file links don't work after saving it to HTML.
# We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
load_options = aw.loading.ChmLoadOptions()
load_options.original_file_name = "amhelp.chm"

with open(MY_DIR + "Document with ms-its links.chm", "rb") as stream:
    doc = aw.Document(stream, load_options)

doc.save(ARTIFACTS_DIR + "ExChmLoadOptions.OriginalFileName.html")
```

### See Also

* module [aspose.words.loading](../../)
* class [ChmLoadOptions](../)

