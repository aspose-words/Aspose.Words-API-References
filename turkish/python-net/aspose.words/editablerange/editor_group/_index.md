---
title: EditableRange.editor_group property
linktitle: editor_group property
articleTitle: editor_group property
second_title: Aspose.Words for Python
description: "EditableRange.editor_group property. Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range."
type: docs
weight: 30
url: /tr/python-net/aspose.words/editablerange/editor_group/
---

## EditableRange.editor_group property

Returns or sets an alias (or editing group) which shall be used to determine if the current user
shall be allowed to edit this editable range.


```python
@property
def editor_group(self) -> aspose.words.EditorType:
    ...

@editor_group.setter
def editor_group(self, value: aspose.words.EditorType):
    ...

```

### Remarks

Single user and editor group cannot be set simultaneously for the specific editable range,
if the one is set, the other will be clear.




### Examples

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " + 'we cannot edit this paragraph without the password.')
# İki iç içe düzenlenebilir aralık oluşturun.
outer_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside the outer editable range and can be edited.')
inner_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside both the outer and inner editable ranges and can be edited.')
# Şu anda, belge oluşturucunun düğüm ekleme imleci birden fazla devam eden düzenlenebilir aralıkta bulunuyor.
# Bu durumda bir düzenlenebilir aralığı sonlandırmak istediğimizde,
# hangi aralığı sonlandırmak istediğimizi, onun EditableRangeStart düğümünü geçirerek belirtmemiz gerekir.
builder.end_editable_range(inner_editable_range_start)
builder.writeln('This paragraph inside the outer editable range and can be edited.')
builder.end_editable_range(outer_editable_range_start)
builder.writeln('This paragraph is outside any editable ranges, and cannot be edited.')
# Bir metin bölgesi, belirtilen gruplara sahip iki üst üste gelen düzenlenebilir aralığa sahipse,
# her iki grup tarafından dışlanan birleşik kullanıcı grubu, metni düzenlemesinin önüne geçilir.
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.Nested.docx')
```

### See Also

* module [aspose.words](../../)
* class [EditableRange](../)

