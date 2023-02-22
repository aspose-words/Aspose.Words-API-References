---
title: ParagraphFormat.Style
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Bu biçimlendirmeye uygulanan paragraf stilini alır veya ayarlar.
type: docs
weight: 330
url: /tr/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Bu biçimlendirmeye uygulanan paragraf stilini alır veya ayarlar.

```csharp
public Style Style { get; set; }
```

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

### Ayrıca bakınız

* class [Style](../../style/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


