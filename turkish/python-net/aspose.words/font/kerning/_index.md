---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /tr/python-net/aspose.words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```python
@property
def kerning(self) -> float:
    ...

@kerning.setter
def kerning(self, value: float):
    ...

```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial Black'
# Oluşturucunun yazı tipi boyutunu ve çekim (kerning) etkili olacak minimum boyutu ayarlayın.
# Yazı tipi boyutu çekim eşiğinin altına düştüğü için, aşağıdaki koşuda çekim uygulanmayacaktır.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Çekim eşiğini, oluşturucunun mevcut yazı tipi boyutu onun üzerinde olacak şekilde ayarlayın.
# Bu noktadan itibaren eklediğimiz tüm metinlere çekim uygulanacak. Karakterler arasındaki boşluklar
# ayarlanacak ve genellikle metin koşusunu biraz daha estetik açıdan hoş bir hale getirecektir.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

