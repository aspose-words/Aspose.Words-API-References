---
title: Enum ParagraphAlignment
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ParagraphAlignment Sıralama. Paragrafta metin hizalamasını belirtir.
type: docs
weight: 4160
url: /tr/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Paragrafta metin hizalamasını belirtir.

```csharp
public enum ParagraphAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Metin sola hizalanır. |
| Center | `1` | Metin yatay olarak ortalanır. |
| Right | `2` | Metin sağa hizalanır. |
| Justify | `3` | Metin hem sola hem de sağa hizalanır. |
| Distributed | `4` | Metin eşit olarak dağıtılır. |
| ArabicMediumKashida | `5` | Yalnızca Arapça. Metin için Kashida uzunluğu, tüketici tarafından belirlenen orta uzunluğa uzatılır. |
| ArabicHighKashida | `7` | Yalnızca Arapça. Metin için Kashida uzunluğu, mümkün olan en geniş uzunluğa uzatılmıştır. |
| ArabicLowKashida | `8` | Yalnızca Arapça. Metin için Kashida uzunluğu biraz daha uzun olacak şekilde uzatıldı. |
| ThaiDistributed | `9` | Yalnızca Tay dili. Metin, Tay dili için bir optimizasyonla hizalanmıştır. |
| MathElementCenterAsGroup | `10` | Bir satırdaki tek Math öğesi, 'Grup Olarak Ortalanmış' olarak hizalanır. |

### Örnekler

Bir Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve alt öğesi olmayan bir belge düğümüyle bitirin.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne alt öğe olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa kurulum özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı var
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünümünü ve içeriğini ayarlayın ve ardından paragrafa alt öğe olarak ekleyin.
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


