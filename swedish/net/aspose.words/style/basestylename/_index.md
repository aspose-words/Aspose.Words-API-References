---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen BaseStyleName för att förbättra din design. Hämta eller ställ enkelt in stilnamnet för förbättrad visuell tilltalning!
type: docs
weight: 30
url: /sv/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Hämtar/ställer in namnet på stilen som stilen är baserad på.

```csharp
public string BaseStyleName { get; set; }
```

## Anmärkningar

Detta blir en tom sträng om stilen inte är baserad på någon annan stil och den kan sättas till en tom sträng.

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
