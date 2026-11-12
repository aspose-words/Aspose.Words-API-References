---
title: Node.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Node.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /tr/python-net/aspose.words/node/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin
# belgenin bazı yapısal öğelerini, örneğin sayfa sonlarını temsil ettiğini gösterir.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# Bir belgeyi dize biçimine dönüştürürken,
# Trim yöntemiyle bazı kontrol karakterlerini atlayabiliriz.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

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

* module [aspose.words](../../)
* class [Node](../)

