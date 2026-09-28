---
title: LoadOptions.msw_version property
linktitle: msw_version property
articleTitle: msw_version property
second_title: Aspose.Words for Python
description: "LoadOptions.msw_version property. Allows to specify that the document loading process should match a specific MS Word version"
type: docs
weight: 100
url: /zh/python-net/aspose.words.loading/loadoptions/msw_version/
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
# 默认情况下，Aspose.Words 按照 Microsoft Word 2019 规范加载文档。
load_options = aw.loading.LoadOptions()
self.assertEqual(aw.settings.MsWordVersion.WORD2019, load_options.msw_version)
# 此文档缺少默认的段落格式样式。
# 当我们使用 Microsoft Word 或 Aspose.Words 加载文档时，将重新生成此默认样式。
load_options.msw_version = aw.settings.MsWordVersion.WORD2007
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
# 按照 Microsoft Word 2007 规范加载时，该样式的行间距将具有此值。
self.assertAlmostEqual(12.95, doc.styles.default_paragraph_format.line_spacing, delta=0.01)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

