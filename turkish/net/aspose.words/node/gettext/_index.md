---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Node GetText yöntem. Bu düğümün ve tüm alt öğelerinin metnini alır C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words/node/gettext/
---
## Node.GetText method

Bu düğümün ve tüm alt öğelerinin metnini alır.

```csharp
public virtual string GetText()
```

## Notlar

Döndürülen dize, yukarıda açıklandığı gibi tüm kontrol ve özel karakterleri içerir.[`ControlChar`](../../controlchar/).

## Örnekler

Kontrol karakterlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin ortaya çıktığını gösterir
// sayfa sonları gibi belgenin bazı yapısal öğelerini temsil eder.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Bir belgeyi string biçimine dönüştürürken,
// Trim metodu ile bazı kontrol karakterlerini atlayabiliriz.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

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

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
