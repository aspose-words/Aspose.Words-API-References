---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: .NET için Aspose.Words
description: Belgelerinizdeki hassas metin hizalaması için Aspose.Words.ParagraphAlignment enum'unu keşfedin. Okunabilirliği ve biçimlendirmeyi kolaylıkla geliştirin!
type: docs
weight: 5130
url: /tr/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Bir paragraftaki metin hizalamasını belirtir.

```csharp
public enum ParagraphAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Metin sola hizalanmıştır. |
| Center | `1` | Metin yatay olarak ortalanır. |
| Right | `2` | Metin sağa hizalanmıştır. |
| Justify | `3` | Metin hem sola hem de sağa hizalanmıştır. |
| Distributed | `4` | Metin eşit olarak dağıtılmıştır. |
| ArabicMediumKashida | `5` | Yalnızca Arapça. Metin için Kashida uzunluğu tüketici tarafından belirlenen orta uzunluğa kadar uzatılır. |
| ArabicHighKashida | `7` | Yalnızca Arapça. Metin için kashidanın uzunluğu mümkün olan en geniş uzunluğa kadar uzatılır. |
| ArabicLowKashida | `8` | Yalnızca Arapça. Metin için Kashida uzunluğu biraz daha uzun olacak şekilde uzatıldı. |
| ThaiDistributed | `9` | Yalnızca Tayca. Metin Tayca için bir optimizasyonla hizalanmıştır. |
| MathElementCenterAsGroup | `10` | Bir satırdaki tek Matematik öğesi, 'Grup Olarak Ortalanmış' olarak hizalanmıştır. |

## Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa düzeni özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluştur, bazı biçimlendirme özelliklerini ayarla ve sonra onu gövdeye bir alt paragraf olarak ekle.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir çalışma oluşturun,
// Görünümünü ve içeriğini ayarlayın ve ardından paragrafın bir alt öğesi olarak ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
