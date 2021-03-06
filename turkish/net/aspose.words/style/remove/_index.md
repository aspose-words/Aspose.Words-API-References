---
title: Remove
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen stili belgeden kaldırır.
type: docs
weight: 180
url: /tr/net/aspose.words/style/remove/
---
## Style.Remove method

Belirtilen stili belgeden kaldırır.

```csharp
public void Remove()
```

### Notlar

Stil kaldırmanın belge modelinde aşağıdaki etkileri vardır:

* Stile yapılan tüm referanslar ilgili paragraflardan, sayılardan ve tablolardan kaldırılır.
* Temel stil kaldırılırsa, biçimlendirmesi alt stillere taşınır.
* Silinecek stilin bağlantılı bir stili varsa, bunların ikisi de silinir.

### Örnekler

Özel bir stilin nasıl oluşturulacağını ve uygulanacağını gösterir.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;

DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki stillerden birini belge oluşturucunun oluşturduğu paragrafa uygulayın.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Özel stilimizi belgenin stiller koleksiyonundan kaldırın.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Kaldırılan bir stil kullanan herhangi bir metin, varsayılan biçimlendirmeye geri döner.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ayrıca bakınız

* class [Style](../../style)
* ad alanı [Aspose.Words](../../style)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
