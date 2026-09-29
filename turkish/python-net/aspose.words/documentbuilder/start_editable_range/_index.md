---
title: DocumentBuilder.start_editable_range method
linktitle: start_editable_range method
articleTitle: start_editable_range method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_editable_range method. Marks the current position in the document as an editable range start."
type: docs
weight: 670
url: /tr/python-net/aspose.words/documentbuilder/start_editable_range/
---

## start_editable_range() {#default}

Marks the current position in the document as an editable range start.


```python
def start_editable_range(self):
    ...
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](./#default) and [DocumentBuilder.end_editable_range()](../end_editable_range/#default)
or [DocumentBuilder.end_editable_range()](../end_editable_range/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# Düzenlenebilir aralıklar, korumalı belgelerin bölümlerini düzenlemeye açık bırakmamıza olanak tanır.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# İyi biçimlendirilmiş bir düzenlenebilir aralık bir başlangıç düğümüne ve bir bitiş düğümüne sahiptir.
# Bu düğümlerin eşleşen kimlikleri vardır ve düzenlenebilir düğümleri kapsar.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Düzenlenebilir aralığın farklı bölümleri birbirine bağlanır.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Her bir bölümün düğüm tiplerine şu şekilde erişebiliriz. Düzenlenebilir aralık kendisi bir düğüm değildir,
# ancak bir başlangıç, bir bitiş ve bunların içerdikleri içerikten oluşan bir varlıktır.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Bir düzenlenebilir aralığı kaldırın. Aralık içindeki tüm düğümler bozulmadan kalır.
editable_range.remove()
```

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
* class [DocumentBuilder](../)

