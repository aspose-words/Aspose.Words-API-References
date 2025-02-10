---
title: ChmLoadOptions constructor
linktitle: ChmLoadOptions constructor
articleTitle: ChmLoadOptions constructor
second_title: Aspose.Words for Python
description: "ChmLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /python-net/aspose.words.loading/chmloadoptions/__init__/
---

## ChmLoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

### Examples

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```python
# Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
# so file links don't work after saving it to HTML.
# We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
load_options = aw.loading.ChmLoadOptions()
load_options.original_file_name = 'amhelp.chm'
doc = aw.Document(stream=io.BytesIO(system_helper.io.File.read_all_bytes(MY_DIR + 'Document with ms-its links.chm')), load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'ExChmLoadOptions.OriginalFileName.html')
```

### See Also

* module [aspose.words.loading](../../)
* class [ChmLoadOptions](../)

