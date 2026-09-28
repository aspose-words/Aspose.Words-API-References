---
title: ChmLoadOptions constructor
linktitle: ChmLoadOptions constructor
articleTitle: ChmLoadOptions constructor
second_title: Aspose.Words for Python
description: "ChmLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /zh/python-net/aspose.words.loading/chmloadoptions/__init__/
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
# 我们的文档包含类似 \"ms-its:amhelp.chm::....htm\" 的 URL，但它的名称不同，
# 因此保存为 HTML 后文件链接无法工作。
# 我们需要在 'ChmLoadOptions' 中定义原始文件名以避免此行为。
load_options = aw.loading.ChmLoadOptions()
load_options.original_file_name = 'amhelp.chm'
doc = aw.Document(stream=io.BytesIO(system_helper.io.File.read_all_bytes(MY_DIR + 'Document with ms-its links.chm')), load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'ExChmLoadOptions.OriginalFileName.html')
```

### See Also

* module [aspose.words.loading](../../)
* class [ChmLoadOptions](../)

