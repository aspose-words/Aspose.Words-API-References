---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words för .NET
description: Upptäck metoden Style Equals för att jämföra inbyggda stilar. Förstå länkade och nästa styckes stilar för förbättrad formatering och designeffektivitet.
type: docs
weight: 220
url: /sv/net/aspose.words/style/equals/
---
## Style.Equals method

Jämförs med den angivna stilen. Stilar ISTD jämförs endast för inbyggda stilar. Standardinställningar för stilar ingår inte i jämförelsen. Basstil, länkad stil och stil för nästa stycke jämförs rekursivt.

```csharp
public bool Equals(Style style)
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
