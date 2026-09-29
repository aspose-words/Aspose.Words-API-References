---
title: Font.small_caps property
linktitle: small_caps property
articleTitle: small_caps property
second_title: Aspose.Words for Python
description: "Font.small_caps property. True if the font is formatted as small capital letters."
type: docs
weight: 370
url: /tr/python-net/aspose.words/font/small_caps/
---

## Font.small_caps property

True if the font is formatted as small capital letters.


```python
@property
def small_caps(self) -> bool:
    ...

@small_caps.setter
def small_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# İçeriği değiştirmeden bir koşulun küçük harf metnini büyük harfe dönüştürmenin iki yolu vardır.
# 1 -  Tüm karakterleri normal büyük harflerde görüntülemek için AllCaps bayrağını ayarlayın:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Tüm karakterleri küçük büyük harflerde (small caps) görüntülemek için SmallCaps bayrağını ayarlayın:
# Bir karakter küçük harf ise, büyük harf biçiminde görünecek
# ancak düşük harf (yazı tipinin x-height'i) ile aynı yüksekliğe sahip olacaktır.
# Başlangıçta büyük harf olan karakterler aynı görünecek.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

