---
title: OdtSaveMeasureUnit enumeration
linktitle: OdtSaveMeasureUnit enumeration
articleTitle: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveMeasureUnit enumeration. Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 530
url: /zh/python-net/aspose.words.saving/odtsavemeasureunit/
---

## OdtSaveMeasureUnit enumeration

Specified units of measure to apply to measurable document content such as shape, widths and other during saving.


### Members

| Name | Description |
| --- | --- |
| CENTIMETERS | Specifies that the document content is saved using centimeters. |
| INCHES | Specifies that the document content is saved using inches. |

### Examples

Shows how to use different measurement units to define style parameters of a saved ODT document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# 当我们将文档导出为 .odt 时，可以使用 OdtSaveOptions 对象来修改文档的保存方式。
# 我们可以将 "MeasureUnit" 属性设置为 "OdtSaveMeasureUnit.Centimeters"
# 以使用公制系统（Open Office 使用的）定义样式参数等内容。
# 我们可以将 "MeasureUnit" 属性设置为 "OdtSaveMeasureUnit.Inches"
# 以使用英制系统（Microsoft Word 使用的系统）来定义内容，例如样式参数。
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

