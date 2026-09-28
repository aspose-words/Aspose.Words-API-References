---
title: OdtSaveOptions.measure_unit property
linktitle: measure_unit property
articleTitle: measure_unit property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.measure_unit property. Allows to specify units of measure to apply to document content"
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/odtsaveoptions/measure_unit/
---

## OdtSaveOptions.measure_unit property

Allows to specify units of measure to apply to document content.
The default value is [OdtSaveMeasureUnit.CENTIMETERS](../../odtsavemeasureunit/#CENTIMETERS)



```python
@property
def measure_unit(self) -> aspose.words.saving.OdtSaveMeasureUnit:
    ...

@measure_unit.setter
def measure_unit(self, value: aspose.words.saving.OdtSaveMeasureUnit):
    ...

```

### Remarks

Open Office uses centimeters when specifying lengths, widths and other measurable formatting and
content properties in documents whereas MS Office uses inches.


### Examples

Shows how to make a saved document conform to an older ODT schema.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = aw.saving.OdtSaveMeasureUnit.CENTIMETERS
save_options.is_strict_schema11 = export_to_odt_11_specs
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt')
self.assertEqual(aw.MeasurementUnits.CENTIMETERS, doc.layout_options.revision_options.measurement_unit)
```

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

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

