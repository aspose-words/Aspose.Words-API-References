---
title: Style.BaseStyleName
second_title: Aspose.Words for .NET API Referansı
description: Style mülk. Bu stilin temel aldığı stilin adını alır/ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Bu stilin temel aldığı stilin adını alır/ayarlar.

```csharp
public string BaseStyleName { get; set; }
```

### Notlar

Stil başka bir stili temel almıyorsa ve boş bir dizeye set olarak ayarlanabiliyorsa, bu boş bir dize olacaktır.

### Örnekler

Stil takma adlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Bu belge "MyStyle,MyStyle Alias 1,MyStyle Alias 2" adında bir stil içeriyor.
// Bir stilin adı virgülle ayrılmış birden fazla değere sahipse, her cümle ayrı bir takma addır.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Bir stile isminin yanı sıra takma adını kullanarak da referans verebiliriz.
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
* ad alanı [Aspose.Words](../../style/)
* toplantı [Aspose.Words](../../../)


