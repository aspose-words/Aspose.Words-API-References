---
title: FieldAutoTextList class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the AUTOTEXTLIST field"
type: docs
weight: 160
url: /python-net/aspose.words.fields/fieldautotextlist/
---

## FieldAutoTextList class

Implements the AUTOTEXTLIST field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.




Creates a shortcut menu based on AutoText entries in the active template.


**Inheritance:** [FieldAutoTextList](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAutoTextList()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_name](./entry_name/) | Gets or sets the name of the AutoText entry. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [list_style](./list_style/) | Gets or sets the name of the style on which the list to contain entries is based. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [screen_tip](./screen_tip/) | Gets or sets the text of the ScreenTip to show. |
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

Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries.

```python
def test_field_auto_text_list(self):

    doc = aw.Document()

    # Create a glossary document and populate it with auto text entries.
    doc.glossary_document = aw.buildingblocks.GlossaryDocument()
    ExField.append_auto_text_entry(doc.glossary_document, "AutoText 1", "Contents of AutoText 1")
    ExField.append_auto_text_entry(doc.glossary_document, "AutoText 2", "Contents of AutoText 2")
    ExField.append_auto_text_entry(doc.glossary_document, "AutoText 3", "Contents of AutoText 3")

    builder = aw.DocumentBuilder(doc)

    # Create an AUTOTEXTLIST field and set the text that the field will display in Microsoft Word.
    # Set the text to prompt the user to right-click this field to select an AutoText building block,
    # whose contents the field will display.
    field = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_TEXT_LIST, True).as_field_auto_text_list()
    field.entry_name = "Right click here to select an AutoText block"
    field.list_style = "Heading 1"
    field.screen_tip = "Hover tip text for AutoTextList goes here"

    self.assertEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.get_field_code())

    doc.save(ARTIFACTS_DIR + "Field.field_auto_text_list.dotx")

@staticmethod
def append_auto_text_entry(glossary_doc: aw.buildingblocks.GlossaryDocument, name: str, contents: str):
    """Create an AutoText-type building block and add it to a glossary document."""

    building_block = aw.buildingblocks.BuildingBlock(glossary_doc)
    building_block.name = name
    building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
    building_block.category = "General"
    building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH

    section = aw.Section(glossary_doc)
    section.append_child(aw.Body(glossary_doc))
    section.body.append_paragraph(contents)
    building_block.append_child(section)

    glossary_doc.append_child(building_block)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

