---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words för .NET
description: Upptäck alla stilalias enkelt med egenskapen Stilalias. Om inga finns får du en tom strängmatris. Förenkla din stilhantering!
type: docs
weight: 10
url: /sv/net/aspose.words/style/aliases/
---
## Style.Aliases property

Hämtar alla alias för denna stil. Om stilen inte har några alias returneras en tom array med sträng.

```csharp
public string[] Aliases { get; }
```

## Exempel

Visar hur man använder stilalias.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Detta dokument innehåller en stil med namnet "MinStil,MinStilAlias1,MinStilAlias2".
// Om ett stilnamn har flera värden separerade med kommatecken, är varje klausul ett separat alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Vi kan referera till en stil med hjälp av dess alias, såväl som dess namn.
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

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
