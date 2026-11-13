---
title: LoadOptions.msw_version property
linktitle: msw_version property
articleTitle: msw_version property
second_title: Aspose.Words for Python
description: "LoadOptions.msw_version property. Allows to specify that the document loading process should match a specific MS Word version"
type: docs
weight: 100
url: /es/python-net/aspose.words.loading/loadoptions/msw_version/
---

## LoadOptions.msw_version property

Allows to specify that the document loading process should match a specific MS Word version.
Default value is [MsWordVersion.WORD2019](../../../aspose.words.settings/mswordversion/#WORD2019)



```python
@property
def msw_version(self) -> aspose.words.settings.MsWordVersion:
    ...

@msw_version.setter
def msw_version(self, value: aspose.words.settings.MsWordVersion):
    ...

```

### Remarks

Different Word versions may handle certain aspects of document content and formatting slightly differently
during the loading process, which may result in minor differences in Document Object Model.


### Examples

Shows how to emulate the loading procedure of a specific Microsoft Word version during document loading.

```python
# Por defecto, Aspose.Words carga documentos según la especificación de Microsoft Word 2019.
load_options = aw.loading.LoadOptions()
self.assertEqual(aw.settings.MsWordVersion.WORD2019, load_options.msw_version)
# Este documento carece del estilo de formato de párrafo predeterminado.
# Este estilo predeterminado se regenerará cuando carguemos el documento ya sea con Microsoft Word o con Aspose.Words.
load_options.msw_version = aw.settings.MsWordVersion.WORD2007
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
# El interlineado del estilo tendrá este valor cuando se cargue según la especificación de Microsoft Word 2007.
self.assertAlmostEqual(12.95, doc.styles.default_paragraph_format.line_spacing, delta=0.01)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

