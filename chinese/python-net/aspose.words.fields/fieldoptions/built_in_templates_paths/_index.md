---
title: FieldOptions.built_in_templates_paths property
linktitle: built_in_templates_paths property
articleTitle: built_in_templates_paths property
second_title: Aspose.Words for Python
description: "FieldOptions.built_in_templates_paths property. Gets or sets paths of MS Word built-in templates."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldoptions/built_in_templates_paths/
---

## FieldOptions.built_in_templates_paths property

Gets or sets paths of MS Word built-in templates.


```python
@property
def built_in_templates_paths(self) -> List[str]:
    ...

@built_in_templates_paths.setter
def built_in_templates_paths(self, value: List[str]):
    ...

```

### Remarks

This property is used by the [FieldAutoText](../../fieldautotext/) and [FieldGlossary](../../fieldglossary/) fields, if referenced auto text entry is not found in the [Document.attached_template](../../../aspose.words/document/attached_template/) template.

By default MS Word stores built-in templates in c:\\Users\\\<username\>\\AppData\\Roaming\\Microsoft\\Document Building Blocks\\1033\\16\\Built-In Building Blocks.dotx and
C:\\Users\\\<username\>\\AppData\\Roaming\\Microsoft\\Templates\\Normal.dotm files.




### Examples

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```python
doc = aw.Document()
# 创建一个术语表文档并向其中添加 AutoText 构件块。
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
building_block = aw.buildingblocks.BuildingBlock(doc.glossary_document)
building_block.name = 'MyBlock'
building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
building_block.category = 'General'
building_block.description = 'MyBlock description'
building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
doc.glossary_document.append_child(building_block)
# 创建一个源并将其作为文本添加到我们的构件块中。
building_block_source = aw.Document()
building_block_source_builder = aw.DocumentBuilder(doc=building_block_source)
building_block_source_builder.writeln('Hello World!')
building_block_content = doc.glossary_document.import_node(src_node=building_block_source.first_section, is_import_children=True)
building_block.append_child(building_block_content)
# 设置一个文件，其中包含我们的文档或其附加模板可能不包含的部分。
doc.field_options.built_in_templates_paths = [MY_DIR + 'Busniess brochure.dotx']
builder = aw.DocumentBuilder(doc=doc)
# 下面是使用字段显示我们构件块内容的两种方法。
# 1 - 使用 AUTOTEXT 字段：
field_auto_text = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_TEXT, update_field=True).as_field_auto_text()
field_auto_text.entry_name = 'MyBlock'
self.assertEqual(' AUTOTEXT  MyBlock', field_auto_text.get_field_code())
# 2 - 使用 GLOSSARY 字段：
field_glossary = builder.insert_field(field_type=aw.fields.FieldType.FIELD_GLOSSARY, update_field=True).as_field_glossary()
field_glossary.entry_name = 'MyBlock'
self.assertEqual(' GLOSSARY  MyBlock', field_glossary.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTOTEXT.GLOSSARY.dotx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

