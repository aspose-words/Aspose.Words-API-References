---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /tr/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




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

Shows how to detect plaintext document text direction.

```python
# "TxtLoadOptions" nesnesi oluşturun, bunu bir belgenin yapıcısına geçirebiliriz
# düz metin belgesini nasıl yüklediğimizi değiştirmek için.
load_options = aw.loading.TxtLoadOptions()
# "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
# Aspose.Words'ün düz metinden yüklediği her paragrafın metin yönünü.
# Her paragrafın "Bidi" özelliği yönünü depolayacak.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# İbranice metni sağdan sola olarak algılayın.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# İngilizce metni sağdan sola olarak algılayın.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

