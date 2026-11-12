---
title: EditableRange.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "EditableRange.remove method. Removes the editable range from the document"
type: docs
weight: 60
url: /tr/python-net/aspose.words/editablerange/remove/
---

## remove() {#default}

Removes the editable range from the document. Does not remove content inside the editable range.


```python
def remove(self):
    ...
```

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

### See Also

* module [aspose.words](../../)
* class [EditableRange](../)

