---
title: PageSetup.line_number_distance_from_text property
linktitle: line_number_distance_from_text property
articleTitle: line_number_distance_from_text property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_distance_from_text property. Gets or sets distance between the right edge of line numbers and the left edge of the document."
type: docs
weight: 220
url: /tr/python-net/aspose.words/pagesetup/line_number_distance_from_text/
---

## PageSetup.line_number_distance_from_text property

Gets or sets distance between the right edge of line numbers and the left edge of the document.


```python
@property
def line_number_distance_from_text(self) -> float:
    ...

@line_number_distance_from_text.setter
def line_number_distance_from_text(self, value: float):
    ...

```

### Remarks

Set this property to zero for automatic distance between the line numbers and text of the document.


### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bölümün PageSetup nesnesini kullanarak bölümün metin satırlarının solunda sayıları gösterebiliriz.
# Bu, bir List nesnesiyle aynı davranıştır,
# ancak tüm bölümü kapsar ve metni hiçbir şekilde değiştirmez.
# Bölümümüz her yeni sayfada numaralandırmayı 1'den yeniden başlatacak ve sayıyı gösterecek,
# eğer 3'ün katıysa, satırın solunda 50pt konumda.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Satır sayacı, "SuppressLineNumbers" bayrağı "true" olarak ayarlanmış herhangi bir paragrafı atlayacaktır.
# Bu paragraf 15. satırda, ki bu 3'ün katıdır ve bu yüzden normalde bir satır numarası gösterirdi.
# Bölümün satır sayacı da bu satırı yok sayacak, sonraki satırı 15. satır olarak ele alacak,
# ve sayımı o noktadan itibaren devam ettirecek.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

