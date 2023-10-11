---
title: Enum ParagraphAlignment
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ParagraphAlignment Sıralama. Bir paragraftaki metin hizalamasını belirtir.
type: docs
weight: 4400
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
| Left | `0` | Metin sola hizalanır. |
| Center | `1` | Metin yatay olarak ortalanır. |
| Right | `2` | Metin sağa hizalanır. |
| Justify | `3` | Metin hem sola hem de sağa hizalanır. |
| Distributed | `4` | Metin eşit olarak dağıtılır. |
| ArabicMediumKashida | `5` | Yalnızca Arapça. Metin için Kashida uzunluğu, tüketici tarafından belirlenen orta uzunluğa kadar genişletilir. |
| ArabicHighKashida | `7` | Yalnızca Arapça. Metin için Kashida uzunluğu mümkün olan en geniş uzunluğa genişletildi. |
| ArabicLowKashida | `8` | Yalnızca Arapça. Metin için Kashida uzunluğu biraz daha uzun olacak şekilde genişletildi. |
| ThaiDistributed | `9` | Yalnızca Tay dili. Metin Tay dili için bir optimizasyonla iki yana yaslanmıştır. |
| MathElementCenterAsGroup | `10` | Bir satırdaki 'Grup Olarak Ortalanmış' olarak hizalanan tek Matematik öğesi. |

### Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümü elde ederiz.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Eğer onu düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Öncelikle yeni bir bölüm oluşturun ve ardından bunu alt öğe olarak kök belge düğümüne ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa yapısı özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünüşünü ve içeriğini ayarlayın ve ardından onu alt öğe olarak paragrafa ekleyin.
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


