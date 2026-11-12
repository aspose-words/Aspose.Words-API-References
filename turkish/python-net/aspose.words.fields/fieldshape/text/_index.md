---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# BIDCOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragrafları numaralar,
# ancak sadece sağdan sola düzenleme dili etkin olduğunda, örneğin İbranice veya Arapça, görünür.
# Aşağıdaki alan ".1" görüntüleyecek; bu, "1." liste numarasının sağdan sola eşdeğeridir.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# İki tane daha BIDCOUTLINE alanı ekleyin; bunlar ".2" ve ".3" görüntüleyecek.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Belgedeki her paragrafın yatay metin hizalamasını RTL olarak ayarlayın.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Microsoft Word'de sağdan sola bir düzenleme dili etkinleştirirsek, alanlarımız sayıları gösterecektir.
# Aksi takdirde, "###" göstereceklerdir.
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Word belgesini açıp Alt+F9 tuşlarına basarsak, bir SHAPE ve bir EMBED alanı göreceğiz.
# Bir SHAPE alanı, "Metin içinde" kaydırma stilinin etkin olduğu bir AutoShape nesnesi için çapa/tuval görevi görür.
# Bir EMBED alanı aynı işlevi görür, ancak gömülü bir nesne için,
# örneğin harici bir Excel belgesinden bir elektronik tablo.
# Ancak, bu alanlar belgenin Fields koleksiyonunda görünmez.
self.assertEqual(0, doc.range.fields.count)
# Bu alanlar yalnızca Microsoft Word'ün eski sürümleri tarafından desteklenir.
# Belge yükleme süreci bu alanları Shape nesnelerine dönüştürecek,
# ki bunlara belgenin düğüm koleksiyonunda erişebiliriz.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# İlk Shape düğümü, giriş belgesindeki SHAPE alanına karşılık gelir,
# bu da AutoShape için satır içi tuvaldir.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# İkinci Shape düğümü, AutoShape'in kendisidir.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Üçüncü Shape, harici elektronik tabloyu içeren EMBED alanıydı.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

