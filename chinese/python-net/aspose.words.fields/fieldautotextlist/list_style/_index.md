---
title: FieldAutoTextList.list_style property
linktitle: list_style property
articleTitle: list_style property
second_title: Aspose.Words for Python
description: "FieldAutoTextList.list_style property. Gets or sets the name of the style on which the list to contain entries is based."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldautotextlist/list_style/
---

## FieldAutoTextList.list_style property

Gets or sets the name of the style on which the list to contain entries is based.


```python
@property
def list_style(self) -> str:
    ...

@list_style.setter
def list_style(self, value: str):
    ...

```

### Examples

Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries.

```python
doc = aw.Document()
# 创建一个术语表文档并使用自动文本条目填充它。
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 1', 'Contents of AutoText 1')
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 2', 'Contents of AutoText 2')
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 3', 'Contents of AutoText 3')
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 AUTOTEXTLIST 字段并设置该字段将在 Microsoft Word 中显示的文本。
# 设置文本以提示用户右键单击此字段以选择 AutoText 构件，
# 该字段将显示其内容。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_TEXT_LIST, update_field=True).as_field_auto_text_list()
field.entry_name = 'Right click here to select an AutoText block'
field.list_style = 'Heading 1'
field.screen_tip = 'Hover tip text for AutoTextList goes here'
self.assertEqual(' AUTOTEXTLIST  "Right click here to select an AutoText block" ' + '\\s "Heading 1" ' + '\\t "Hover tip text for AutoTextList goes here"', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTOTEXTLIST.dotx')
```

Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries (AppendAutoTextEntry).

```python
@staticmethod
def _append_auto_text_entry(glossary_doc, name, contents):
    building_block = aw.buildingblocks.BuildingBlock(glossary_doc)
    building_block.name = name
    building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
    building_block.category = 'General'
    building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
    section = aw.Section(glossary_doc)
    section.append_child(aw.Body(glossary_doc))
    section.body.append_paragraph(contents)
    building_block.append_child(section)
    glossary_doc.append_child(building_block)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoTextList](../)

