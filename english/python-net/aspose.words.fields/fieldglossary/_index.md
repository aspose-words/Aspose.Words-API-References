﻿---
title: FieldGlossary class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the GLOSSARY field"
type: docs
weight: 500
url: /python-net/aspose.words.fields/fieldglossary/
---

## FieldGlossary class

Implements the GLOSSARY field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts a glossary entry.


**Inheritance:** [FieldGlossary](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldGlossary()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_name](./entry_name/) | Gets or sets the name of the glossary entry to insert. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

