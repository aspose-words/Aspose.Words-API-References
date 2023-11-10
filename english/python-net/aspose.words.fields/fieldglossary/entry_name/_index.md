---
title: FieldGlossary.entry_name property
linktitle: entry_name property
articleTitle: entry_name property
second_title: Aspose.Words for Python
description: "FieldGlossary.entry_name property. Gets or sets the name of the glossary entry to insert."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldglossary/entry_name/
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

# Create a glossary document and add an AutoText building block to it.
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
building_block = aw.buildingblocks.BuildingBlock(doc.glossary_document)
building_block.name = "MyBlock"
building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
building_block.category = "General"
building_block.description = "MyBlock description"
building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
doc.glossary_document.append_child(building_block)

# Create a source and add it as text to our building block.
building_block_source = aw.Document()
building_block_source_builder = aw.DocumentBuilder(building_block_source)
building_block_source_builder.writeln("Hello World!")

building_block_content = doc.glossary_document.import_node(building_block_source.first_section, True)
building_block.append_child(building_block_content)

# Set a file which contains parts that our document, or its attached template may not contain.
doc.field_options.built_in_templates_paths = [MY_DIR + "Busniess brochure.dotx"]

builder = aw.DocumentBuilder(doc)

# Below are two ways to use fields to display the contents of our building block.
# 1 -  Using an AUTOTEXT field:
field_auto_text = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_TEXT, True).as_field_auto_text()
field_auto_text.entry_name = "MyBlock"

self.assertEqual(" AUTOTEXT  MyBlock", field_auto_text.get_field_code())

# 2 -  Using a GLOSSARY field:
field_glossary = builder.insert_field(aw.fields.FieldType.FIELD_GLOSSARY, True).as_field_glossary()
field_glossary.entry_name = "MyBlock"

self.assertEqual(" GLOSSARY  MyBlock", field_glossary.get_field_code())

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_auto_text.glossary.dotx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldGlossary](../)

