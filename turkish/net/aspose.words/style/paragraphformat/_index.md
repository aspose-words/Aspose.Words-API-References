---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: .NET için Aspose.Words
description: Gelişmiş belge sunumu ve profesyonel biçimlendirme için stillerin paragraf biçimlendirmesine nasıl erişeceğinizi ve bunları nasıl özelleştireceğinizi keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Stilin paragraf biçimlendirmesini alır.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Notlar

Karakter ve liste stilleri için bu özellik şunu döndürür:`hükümsüz`.

## Örnekler

Liste biçimlendirmesiyle bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
