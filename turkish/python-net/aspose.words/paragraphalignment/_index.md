---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 970
url: /tr/python-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| LEFT | Text is aligned to the left. |
| CENTER | Text is centered horizontally. |
| RIGHT | Text is aligned to the right. |
| JUSTIFY | Text is aligned to both left and right. |
| DISTRIBUTED | Text is evenly distributed. |
| ARABIC_MEDIUM_KASHIDA | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ARABIC_HIGH_KASHIDA | Arabic only. Kashida length for text is extended to its widest possible length. |
| ARABIC_LOW_KASHIDA | Arabic only. Kashida length for text is extended to a slightly longer length. |
| THAI_DISTRIBUTED | Thai only. Text is justified with an optimization for Thai. |
| MATH_ELEMENT_CENTER_AS_GROUP | The only Math element in a line, aligned as 'Centered As Group'. |

### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
# "RemoveAllChildren" metodunu çağırarak bu düğümlerin tümünü kaldırın,
# ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc.remove_all_children()
# Bu belge artık içerik ekleyebileceğimiz birleşik çocuk düğümlerine sahip değil.
# Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
# İlk olarak yeni bir bölüm oluşturun ve ardından bunu kök belge düğümüne çocuk olarak ekleyin.
section = aw.Section(doc)
doc.append_child(section)
# Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Bir bölüm bir gövdeye ihtiyaç duyar; bu gövde tüm içeriğini barındırır ve gösterir
# sayfada bölümün başlığı ile altbilgisi arasında.
body = aw.Body(doc)
section.append_child(body)
# Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından gövdeye çocuk olarak ekleyin.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Son olarak, belgeyi oluşturmak için bazı içerikler ekleyin. Bir run oluşturun,
# görünümünü ve içeriğini ayarlayın, ardından paragrafın çocuğu olarak ekleyin.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)

