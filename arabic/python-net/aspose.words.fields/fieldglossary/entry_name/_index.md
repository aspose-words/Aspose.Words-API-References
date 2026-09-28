---
title: FieldGlossary.entry_name property
linktitle: entry_name property
articleTitle: entry_name property
second_title: Aspose.Words for Python
description: "FieldGlossary.entry_name property. Gets or sets the name of the glossary entry to insert."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldglossary/entry_name/
---

## FieldGlossary.entry_name property

Gets or sets the name of the glossary entry to insert.


```python
@property
def entry_name(self) -> str:
    ...

@entry_name.setter
def entry_name(self, value: str):
    ...

```

### Examples

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```python
doc = aw.Document()
# أنشئ مستند مسرد وأضف إليه كتلة بناء AutoText.
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
building_block = aw.buildingblocks.BuildingBlock(doc.glossary_document)
building_block.name = 'MyBlock'
building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
building_block.category = 'General'
building_block.description = 'MyBlock description'
building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
doc.glossary_document.append_child(building_block)
# أنشئ مصدرًا وأضفه كنص إلى كتلة البناء الخاصة بنا.
building_block_source = aw.Document()
building_block_source_builder = aw.DocumentBuilder(doc=building_block_source)
building_block_source_builder.writeln('Hello World!')
building_block_content = doc.glossary_document.import_node(src_node=building_block_source.first_section, is_import_children=True)
building_block.append_child(building_block_content)
# حدد ملفًا يحتوي على أجزاء قد لا يحتويها مستندنا أو القالب المرفق به.
doc.field_options.built_in_templates_paths = [MY_DIR + 'Busniess brochure.dotx']
builder = aw.DocumentBuilder(doc=doc)
# فيما يلي طريقتان لاستخدام الحقول لعرض محتويات كتلة البناء الخاصة بنا.
# 1 -  استخدام حقل AUTOTEXT:
field_auto_text = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_TEXT, update_field=True).as_field_auto_text()
field_auto_text.entry_name = 'MyBlock'
self.assertEqual(' AUTOTEXT  MyBlock', field_auto_text.get_field_code())
# 2 -  استخدام حقل GLOSSARY:
field_glossary = builder.insert_field(field_type=aw.fields.FieldType.FIELD_GLOSSARY, update_field=True).as_field_glossary()
field_glossary.entry_name = 'MyBlock'
self.assertEqual(' GLOSSARY  MyBlock', field_glossary.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTOTEXT.GLOSSARY.dotx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldGlossary](../)

