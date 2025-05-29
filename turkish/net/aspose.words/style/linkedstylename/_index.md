---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: .NET için Aspose.Words
description: LinkedStyleName özelliğini nasıl biçimlendireceğinizi, bağlantılı stilleri nasıl kolayca yöneteceğinizi ve sorunsuz entegrasyonla tasarım iş akışınızı nasıl geliştireceğinizi keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Adını alır/ayarlar[`Style`](../) buna bağlı. Hiçbir stil bağlı değilse boş dize döndürür.

```csharp
public string LinkedStyleName { get; set; }
```

## Notlar

Sadece paragraf stilini karakter stiline, tersini de paragraf stiline bağlamak mümkündür.

Mevcut stil için LinkedStyleName ayarlanması, otomatik olarak bağlantılı stil için LinkedStyleName ayarlanmasına yol açar.

Boş dizeyi atamak, daha önce bağlanmış olan stilin bağlantısını kaldırmaya eşdeğerdir.

## Örnekler

Stillerin kendi aralarında nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

Stil takma adlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Bu belge "MyStyle,MyStyle Alias 1,MyStyle Alias 2" adında bir stil içeriyor.
// Bir stilin adı virgülle ayrılmış birden fazla değere sahipse, her bir cümle ayrı bir takma addır.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Bir stile isminin yanı sıra takma adını kullanarak da başvurabiliriz.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
