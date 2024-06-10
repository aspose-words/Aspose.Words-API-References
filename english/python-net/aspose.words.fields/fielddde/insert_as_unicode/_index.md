---
title: FieldDde.insert_as_unicode property
linktitle: insert_as_unicode property
articleTitle: insert_as_unicode property
second_title: Aspose.Words for Python
description: "FieldDde.insert_as_unicode property. Gets or sets whether to insert the linked object as Unicode text."
type: docs
weight: 80
url: /python-net/aspose.words.fields/fielddde/insert_as_unicode/
---

## FieldDde.insert_as_unicode property

Gets or sets whether to insert the linked object as Unicode text.


```python
@property
def insert_as_unicode(self) -> bool:
    ...

@insert_as_unicode.setter
def insert_as_unicode(self, value: bool):
    ...

```

### Examples

Shows how to use various field types to link to other documents in the local file system, and display their contents.

```python
def field_linked_objects_as_text():
    for insert_linked_object_as in (InsertLinkedObjectAs.TEXT, InsertLinkedObjectAs.UNICODE, InsertLinkedObjectAs.HTML, InsertLinkedObjectAs.RTF):
        with self.subTest(insert_linked_object_as=insert_linked_object_as):
            doc = aw.Document()
            builder = aw.DocumentBuilder(doc)
            # Below are three types of fields we can use to display contents from a linked document in the form of text.
            # 1 -  A LINK field:
            builder.writeln('FieldLink:\n')
            insert_field_link(builder, insert_linked_object_as, 'Word.document.8', MY_DIR + 'Document.docx', None, True)
            # 2 -  A DDE field:
            builder.writeln('FieldDde:\n')
            insert_field_fde(builder, insert_linked_object_as, 'Excel.Sheet', MY_DIR + 'Spreadsheet.xlsx', 'Sheet1!R1C1', True, True)
            # 3 -  A DDEAUTO field:
            builder.writeln('FieldDdeAuto:\n')
            insert_field_fde_auto(builder, insert_linked_object_as, 'Excel.Sheet', MY_DIR + 'Spreadsheet.xlsx', 'Sheet1!R1C1', True)
            doc.update_fields()
            doc.save(ARTIFACTS_DIR + 'Field.field_linked_objects_as_text.docx')

def field_linked_objects_as_image():
    for insert_linked_object_as in (InsertLinkedObjectAs.PICTURE, InsertLinkedObjectAs.BITMAP):
        with self.subTest(insert_linked_object_as=insert_linked_object_as):
            doc = aw.Document()
            builder = aw.DocumentBuilder(doc)
            # Below are three types of fields we can use to display contents from a linked document in the form of an image.
            # 1 -  A LINK field:
            builder.writeln('FieldLink:\n')
            insert_field_link(builder, insert_linked_object_as, 'Excel.Sheet', MY_DIR + 'MySpreadsheet.xlsx', 'Sheet1!R2C2', True)
            # 2 -  A DDE field:
            builder.writeln('FieldDde:\n')
            insert_field_fde(builder, insert_linked_object_as, 'Excel.Sheet', MY_DIR + 'Spreadsheet.xlsx', 'Sheet1!R1C1', True, True)
            # 3 -  A DDEAUTO field:
            builder.writeln('FieldDdeAuto:\n')
            insert_field_fde_auto(builder, insert_linked_object_as, 'Excel.Sheet', MY_DIR + 'Spreadsheet.xlsx', 'Sheet1!R1C1', True)
            doc.update_fields()
            doc.save(ARTIFACTS_DIR + 'Field.field_linked_objects_as_image.docx')

def insert_field_link(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs', prog_id: str, source_full_name: str, source_item: str, should_auto_update: bool):
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
    builder.writeln('\n')

def insert_field_fde(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs', prog_id: str, source_full_name: str, source_item: str, is_linked: bool, should_auto_update: bool):
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
    builder.writeln('\n')

def insert_field_fde_auto(builder: aw.DocumentBuilder, insert_linked_object_as: 'ExField.InsertLinkedObjectAs', prog_id: str, source_full_name: str, source_item: str, is_linked: bool):
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

* module [aspose.words.fields](../../)
* class [FieldDde](../)

