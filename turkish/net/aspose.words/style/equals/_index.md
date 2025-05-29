---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: .NET için Aspose.Words
description: Yerleşik stilleri karşılaştırmak için Style Equals yöntemini keşfedin. Gelişmiş biçimlendirme ve tasarım verimliliği için bağlantılı ve sonraki paragraf stillerini anlayın.
type: docs
weight: 220
url: /tr/net/aspose.words/style/equals/
---
## Style.Equals method

Belirtilen stille karşılaştırılır. Stil Istd'leri yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlantılı stil ve sonraki paragraf stili yinelemeli olarak karşılaştırılır.

```csharp
public bool Equals(Style style)
```

## Örnekler

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
