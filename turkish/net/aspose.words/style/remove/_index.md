---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Style Remove yöntemi ile istenmeyen stilleri belgenizden zahmetsizce ortadan kaldırın. İçeriğinizin görünümünü geliştirin ve tutarlılığı koruyun!
type: docs
weight: 230
url: /tr/net/aspose.words/style/remove/
---
## Style.Remove method

Belirtilen stili belgeden kaldırır.

```csharp
public void Remove()
```

## Notlar

Stil kaldırmanın belge modeli üzerinde şu etkileri vardır:

* Stile ilişkin tüm referanslar ilgili paragraflardan, bölümlerden ve tablolardan kaldırılmıştır.
* Temel stil kaldırılırsa biçimlendirmesi alt stillere taşınır.
* Silinecek stilin bağlantılı bir stili varsa her ikisi de silinir.

## Örnekler

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Stili otomatik olarak yeniden tanımla.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun oluşturduğu paragrafa, belgedeki stillerden birini uygula.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Özel stilimizi belgenin stiller koleksiyonundan kaldıralım.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Kaldırılan bir stili kullanan herhangi bir metin varsayılan biçimlendirmeye geri döner.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
