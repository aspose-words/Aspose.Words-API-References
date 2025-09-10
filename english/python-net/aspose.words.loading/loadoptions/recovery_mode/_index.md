---
title: LoadOptions.recovery_mode property
linktitle: recovery_mode property
articleTitle: recovery_mode property
second_title: Aspose.Words for Python
description: "LoadOptions.recovery_mode property. Defines how the document should be handled if errors occur during loading"
type: docs
weight: 140
url: /python-net/aspose.words.loading/loadoptions/recovery_mode/
---

## LoadOptions.recovery_mode property

Defines how the document should be handled if errors occur during loading.  
Use this property to specify whether the system should attempt to recover the document 
or follow another defined behavior.  
The default value is [DocumentRecoveryMode.TRY_RECOVER](../../documentrecoverymode/#TRY_RECOVER). 



```python
@property
def recovery_mode(self) -> aspose.words.loading.DocumentRecoveryMode:
    ...

@recovery_mode.setter
def recovery_mode(self, value: aspose.words.loading.DocumentRecoveryMode):
    ...

```

### Examples

Shows how to try to recover a document if errors occurred during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.recovery_mode = aw.loading.DocumentRecoveryMode.TRY_RECOVER
doc = aw.Document(file_name=MY_DIR + 'Corrupted footnotes.docx', load_options=load_options)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

