---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /tr/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# İkinci ve üçüncü paragrafların metniyle başlayan büyük bir harf içeren bir paragraf ekleyin.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Şu anda, ikinci ve üçüncü paragraflar birincinin altında görünecek.
# İlk paragrafı, diğer paragraflar için bir drop cap (büyük harf) olarak, "ParagraphFormat" nesnesi aracılığıyla dönüştürebiliriz.
# "DropCapPosition" özelliğini "DropCapPosition.Margin" olarak ayarlayın, drop cap'i yerleştirmek için
# metnimiz soldan sağa ise sayfanın sol kenar boşluğunun dışına.
# "DropCapPosition" özelliğini "DropCapPosition.Normal" olarak ayarlayın, drop cap'i sayfa kenar boşlukları içinde yerleştirmek için
# ve geri kalan metni onun etrafına sarmak için.
# "DropCapPosition.None" tüm paragraflar için varsayılan durumdur.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

