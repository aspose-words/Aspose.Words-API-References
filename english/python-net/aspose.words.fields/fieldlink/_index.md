---
title: FieldLink class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the LINK field."
type: docs
weight: 650
url: /python-net/aspose.words.fields/fieldlink/
---

## FieldLink class

Implements the LINK field.


For information copied from another application, this field links that information to its original
source file.


**Inheritance:** [FieldLink](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldLink()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [auto_update](./auto_update/) | Gets or sets whether to update this field automatically. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [format_update_type](./format_update_type/) | Gets or sets a way the linked object updates its formatting. |
| [insert_as_bitmap](./insert_as_bitmap/) | Gets or sets whether to insert the linked object as a bitmap. |
| [insert_as_html](./insert_as_html/) | Gets or sets whether to insert the linked object as HTML format text. |
| [insert_as_picture](./insert_as_picture/) | Gets or sets whether to insert the linked object as a picture. |
| [insert_as_rtf](./insert_as_rtf/) | Gets or sets whether to insert the linked object in rich-text format (RTF). |
| [insert_as_text](./insert_as_text/) | Gets or sets whether to insert the linked object in text-only format. |
| [insert_as_unicode](./insert_as_unicode/) | Gets or sets whether to insert the linked object as Unicode text. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_linked](./is_linked/) | Gets or sets whether to reduce the file size by not storing graphics data with the document. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [prog_id](./prog_id/) | Gets or sets the application type of the link information. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [source_full_name](./source_full_name/) | Gets or sets the name and location of the source file. |
| [source_item](./source_item/) | Gets or sets the portion of the source file that's being linked. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use various field types to link to other documents in the local file system, and display their contents.

```python
def test_field_linked_objects_as_text(self):

    for insert_linked_object_as in (ExField.InsertLinkedObjectAs.TEXT,
                                    ExField.InsertLinkedObjectAs.UNICODE,
                                    ExField.InsertLinkedObjectAs.HTML,
                                    ExField.InsertLinkedObjectAs.RTF):
        with self.subTest(insert_linked_object_as=insert_linked_object_as):
            doc = aw.Document()
            builder = aw.DocumentBuilder(doc)

            # Below are three types of fields we can use to display contents from a linked document in the form of text.
            # 1 -  A LINK field:
            builder.writeln("FieldLink:\n")
            ExField.insert_field_link(builder, insert_linked_object_as, "Word.document.8", MY_DIR + "Document.docx", None, True)

            # 2 -  A DDE field:
            builder.writeln("FieldDde:\n")
            ExField.insert_field_fde(builder, insert_linked_object_as, "Excel.Sheet", MY_DIR + "Spreadsheet.xlsx",
                "Sheet1!R1C1", True, True)

            # 3 -  A DDEAUTO field:
            builder.writeln("FieldDdeAuto:\n")
            ExField.insert_field_fde_auto(builder, insert_linked_object_as, "Excel.Sheet", MY_DIR + "Spreadsheet.xlsx",
                "Sheet1!R1C1", True)

            doc.update_fields()
            doc.save(ARTIFACTS_DIR + "Field.field_linked_objects_as_text.docx")

def test_field_linked_objects_as_image(self):

    for insert_linked_object_as in (ExField.InsertLinkedObjectAs.PICTURE,
                                    ExField.InsertLinkedObjectAs.BITMAP):
        with self.subTest(insert_linked_object_as=insert_linked_object_as):
            doc = aw.Document()
            builder = aw.DocumentBuilder(doc)

            # Below are three types of fields we can use to display contents from a linked document in the form of an image.
            # 1 -  A LINK field:
            builder.writeln("FieldLink:\n")
            ExField.insert_field_link(builder, insert_linked_object_as, "Excel.Sheet", MY_DIR + "MySpreadsheet.xlsx",
                "Sheet1!R2C2", True)

            # 2 -  A DDE field:
            builder.writeln("FieldDde:\n")
            ExField.insert_field_fde(builder, insert_linked_object_as, "Excel.Sheet", MY_DIR + "Spreadsheet.xlsx",
                "Sheet1!R1C1", True, True)

            # 3 -  A DDEAUTO field:
            builder.writeln("FieldDdeAuto:\n")
            ExField.insert_field_fde_auto(builder, insert_linked_object_as, "Excel.Sheet", MY_DIR + "Spreadsheet.xlsx",
                "Sheet1!R1C1", True)

            doc.update_fields()
            doc.save(ARTIFACTS_DIR + "Field.field_linked_objects_as_image.docx")

@staticmethod
def insert_field_link(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs',
    prog_id: str, source_full_name: str, source_item: str, should_auto_update: bool):
    """ExField.InsertLinkedObjectAs.BITMAP"""

    field = builder.insert_field(aw.fields.FieldType.FIELD_LINK, True).as_field_link()

    if insert_linked_object_as == ExField.InsertLinkedObjectAs.TEXT:
        field.insert_as_text = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.UNICODE:
        field.insert_as_unicode = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.HTML:
        field.insert_as_html = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.RTF:
        field.insert_as_rtf = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.PICTURE:
        field.insert_as_picture = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.BITMAP:
        field.insert_as_bitmap = True

    field.auto_update = should_auto_update
    field.prog_id = prog_id
    field.source_full_name = source_full_name
    field.source_item = source_item

    builder.writeln("\n")

@staticmethod
def insert_field_fde(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs', prog_id: str,
    source_full_name: str, source_item: str, is_linked: bool, should_auto_update: bool):
    """Use a document builder to insert a DDE field, and set its properties according to parameters."""

    field = builder.insert_field(aw.fields.FieldType.FIELD_DDE, True).as_field_dde()

    if insert_linked_object_as == ExField.InsertLinkedObjectAs.TEXT:
        field.insert_as_text = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.UNICODE:
        field.insert_as_unicode = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.HTML:
        field.insert_as_html = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.RTF:
        field.insert_as_rtf = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.PICTURE:
        field.insert_as_picture = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.BITMAP:
        field.insert_as_bitmap = True

    field.auto_update = should_auto_update
    field.prog_id = prog_id
    field.source_full_name = source_full_name
    field.source_item = source_item
    field.is_linked = is_linked

    builder.writeln("\n")

@staticmethod
def insert_field_fde_auto(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs',
    prog_id: str, source_full_name: str, source_item: str, is_linked: bool):
    """Use a document builder to insert a DDEAUTO, field and set its properties according to parameters."""

    field = builder.insert_field(aw.fields.FieldType.FIELD_DDEAUTO, True).as_field_dde_auto()

    if insert_linked_object_as == ExField.InsertLinkedObjectAs.TEXT:
        field.insert_as_text = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.UNICODE:
        field.insert_as_unicode = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.HTML:
        field.insert_as_html = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.RTF:
        field.insert_as_rtf = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.PICTURE:
        field.insert_as_picture = True

    elif insert_linked_object_as == ExField.InsertLinkedObjectAs.BITMAP:
        field.insert_as_bitmap = True

    field.prog_id = prog_id
    field.source_full_name = source_full_name
    field.source_item = source_item
    field.is_linked = is_linked

class InsertLinkedObjectAs(Enum):

    # LinkedObjectAsText
    TEXT = 1
    UNICODE = 2
    HTML = 3
    RTF = 4
    # LinkedObjectAsImage
    PICTURE = 5
    BITMAP = 6
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

