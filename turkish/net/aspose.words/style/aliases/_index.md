---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: .NET için Aspose.Words
description: Style Aliases özelliğiyle tüm stil takma adlarını zahmetsizce keşfedin. Hiçbiri yoksa, boş bir dize dizisi alın. Stil yönetiminizi basitleştirin!
type: docs
weight: 10
url: /tr/net/aspose.words/style/aliases/
---
## Style.Aliases property

Bu stilin tüm takma adlarını alır. Stilin takma adı yoksa boş bir dize dizisi döndürülür.

```csharp
public string[] Aliases { get; }
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
