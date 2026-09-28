---
title: ChmLoadOptions constructor
linktitle: ChmLoadOptions constructor
articleTitle: ChmLoadOptions constructor
second_title: Aspose.Words for Python
description: "ChmLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /fr/python-net/aspose.words.loading/chmloadoptions/__init__/
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
# Notre document contient des URL comme "ms-its:amhelp.chm::....htm", mais il a un nom différent,
# ainsi les liens de fichiers ne fonctionnent pas après l'avoir enregistré en HTML.
# Nous devons définir le nom de fichier original dans 'ChmLoadOptions' pour éviter ce comportement.
load_options = aw.loading.ChmLoadOptions()
load_options.original_file_name = 'amhelp.chm'
doc = aw.Document(stream=io.BytesIO(system_helper.io.File.read_all_bytes(MY_DIR + 'Document with ms-its links.chm')), load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'ExChmLoadOptions.OriginalFileName.html')
```

### See Also

* module [aspose.words.loading](../../)
* class [ChmLoadOptions](../)

