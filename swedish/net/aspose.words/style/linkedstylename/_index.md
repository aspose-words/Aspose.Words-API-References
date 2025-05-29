---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words för .NET
description: Upptäck hur du formaterar egenskapen LinkedStyleName, enkelt hanterar länkade stilar och förbättrar ditt designarbetsflöde med sömlös integration.
type: docs
weight: 90
url: /sv/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Hämtar/ställer in namnet på[`Style`](../) länkad till denna. Returnerar en tom sträng om inga stilar är länkade.

```csharp
public string LinkedStyleName { get; set; }
```

## Anmärkningar

Det är bara tillåtet att länka styckeformatet till teckenformatet och vice versa.

Om du anger LinkedStyleName för den aktuella stilen leder det automatiskt till att LinkedStyleName anges för den länkade stilen.

Att tilldela den tomma strängen är liktydigt med att ta bort länken till den tidigare länkade stilen.

## Exempel

Visar hur man länkar stilar sinsemellan.

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
