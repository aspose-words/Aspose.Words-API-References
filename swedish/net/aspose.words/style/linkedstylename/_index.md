---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words för .NET
description: Style LinkedStyleName fast egendom. Hämtar namnet påStyle kopplat till denna. Returnerar tom sträng om inga stilar är länkade i C#.
type: docs
weight: 90
url: /sv/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Hämtar namnet på[`Style`](../) kopplat till denna. Returnerar tom sträng om inga stilar är länkade.

```csharp
public string LinkedStyleName { get; }
```

## Exempel

Visar hur man använder stilalias.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Det här dokumentet innehåller en stil som heter "MyStyle, MyStyle Alias 1, MyStyle Alias 2".
// Om en stils namn har flera värden separerade med kommatecken, är varje sats ett separat alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Vi kan referera till en stil med dess alias, såväl som dess namn.
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
