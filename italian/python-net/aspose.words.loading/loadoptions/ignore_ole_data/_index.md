---
title: LoadOptions.ignore_ole_data property
linktitle: ignore_ole_data property
articleTitle: ignore_ole_data property
second_title: Aspose.Words for Python
description: "LoadOptions.ignore_ole_data property. Specifies whether to ignore the OLE data."
type: docs
weight: 70
url: /it/python-net/aspose.words.loading/loadoptions/ignore_ole_data/
---

## LoadOptions.ignore_ole_data property

Specifies whether to ignore the OLE data.


```python
@property
def ignore_ole_data(self) -> bool:
    ...

@ignore_ole_data.setter
def ignore_ole_data(self, value: bool):
    ...

```

### Remarks

Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is ``False``.




### Examples

Shows how to ingore OLE data while loading.

```python
# Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni
# senza perdita di dati nel caso in cui il formato di destinazione non supporti oggetti OLE.
load_options = aw.loading.LoadOptions()
load_options.ignore_ole_data = True
doc = aw.Document(file_name=MY_DIR + 'OLE objects.docx', load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'LoadOptions.IgnoreOleData.docx')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

