---
title: Style.Font
second_title: Aspose.Words for .NET API Referansı
description: Style mülk. Stilin karakter biçimlendirmesini alır.
type: docs
weight: 50
url: /tr/net/aspose.words/style/font/
---
## Style.Font property

Stilin karakter biçimlendirmesini alır.

```csharp
public Font Font { get; }
```

### Notlar

Liste stilleri için bu özellik null değerini döndürür.

### Örnekler

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Özel bir paragraf stili oluşturun.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanacağından emin olun.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Paragraf stilini belge oluşturucunun geçerli paragrafına uygulayın ve ardından biraz metin ekleyin.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stille değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

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

* class [Font](../../font/)
* class [Style](../)
* ad alanı [Aspose.Words](../../style/)
* toplantı [Aspose.Words](../../../)


