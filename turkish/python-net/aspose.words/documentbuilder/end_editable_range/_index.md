---
title: DocumentBuilder.end_editable_range method
linktitle: end_editable_range method
articleTitle: end_editable_range method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.end_editable_range method"
type: docs
weight: 230
url: /tr/python-net/aspose.words/documentbuilder/end_editable_range/
---

## end_editable_range() {#default}

Marks the current position in the document as an editable range end.


```python
def end_editable_range(self):
    ...
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](../start_editable_range/#default) and [DocumentBuilder.end_editable_range()](./#default)
or [DocumentBuilder.end_editable_range()](./#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range end node that was just created.


## end_editable_range(start) {#editablerangestart}

Marks the current position in the document as an editable range end.


```python
def end_editable_range(self, start: aspose.words.EditableRangeStart):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| start | [EditableRangeStart](../../editablerangestart/) | This editable range start. |

### Remarks

Use this overload during creating nested editable ranges.

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](../start_editable_range/#default) and [DocumentBuilder.end_editable_range()](./#default)
or [DocumentBuilder.end_editable_range()](./#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range end node that was just created.


## Examples

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

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

