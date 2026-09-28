---
title: FieldRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldRef.bookmark_name property. Gets or sets the referenced bookmark's name."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldref/bookmark_name/
---

## FieldRef.bookmark_name property

Gets or sets the referenced bookmark's name.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to insert REF fields to reference bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #1')
builder.write('Text that will appear in REF field')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #2')
builder.end_bookmark('MyBookmark')
builder.move_to_document_start()
# سنطبق تنسيق قائمة مخصص، حيث يشير عدد الأقواس الزاوية إلى مستوى القائمة الحالي.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# أدرج حقل REF سيحتوي على النص داخل علامتنا المرجعية، يعمل كرابط تشعبي، وينسخ حواشي العلامة المرجعية.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# أدرج حقل REF، وعرض ما إذا كانت العلامة المرجعية المشار إليها فوقه أم تحته.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# اعرض رقم القائمة للعلامة المرجعية كما يظهر في المستند.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# اعرض رقم قائمة العلامة المرجعية، لكن مع حذف الأحرف غير الفاصلة، مثل الأقواس الزاوية.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# انتقل إلى مستوى قائمة أدنى.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# اعرض رقم قائمة العلامة المرجعية وأرقام جميع مستويات القائمة التي فوقها.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# اعرض أرقام مستويات القائمة بين حقل REF هذا والعلامة المرجعية التي يشير إليها.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# في نهاية المستند، ستظهر العلامة المرجعية كعنصر قائمة هنا.
builder.writeln('List level above bookmark')
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>>> \x02'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.REF.docx')
```

Shows how to insert REF fields to reference bookmarks (InsertFieldRef).

```python
@staticmethod
def _insert_field_ref(builder, bookmark_name, text_before, text_after):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
    field.bookmark_name = bookmark_name
    builder.write(text_after)
    return field
```

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# تسمية النص المؤشر عليه بعلامة مرجعية باستخدام حقل SET.
# يشير هذا الحقل إلى "bookmark" وليس إلى بنية علامة مرجعية تظهر داخل النص، بل إلى متغيّر مسمى.
field_set = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SET, update_field=False).as_field_set()
field_set.bookmark_name = 'MyBookmark'
field_set.bookmark_text = 'Hello world!'
field_set.update()
self.assertEqual(' SET  MyBookmark "Hello world!"', field_set.get_field_code())
# أشر إلى العلامة المرجعية بالاسم في حقل REF وعرض محتوياتها.
field_ref = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
field_ref.bookmark_name = 'MyBookmark'
field_ref.update()
self.assertEqual(' REF  MyBookmark', field_ref.get_field_code())
self.assertEqual('Hello world!', field_ref.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.SET.REF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

