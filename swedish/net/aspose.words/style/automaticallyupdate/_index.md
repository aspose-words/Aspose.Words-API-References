---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words för .NET
description: Style AutomaticallyUpdate fast egendom. Anger om denna stil automatiskt omdefinieras baserat på lämpligt värde i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Anger om denna stil automatiskt omdefinieras baserat på lämpligt värde.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Anmärkningar

Om egenskapsvärdet är satt till true, omdefinierar MS Word automatiskt den aktuella stilen när lämplig styckeformatering har ändrats.

Egenskapen AutomaticallyUpdate är endast tillämplig på styckeformat.

Standardvärdet är`falsk`.

## Exempel

Visar hur man skapar och tillämpar en anpassad stil.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Omdefiniera stil automatiskt.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Tillämpa en av stilarna från dokumentet på stycket som dokumentbyggaren skapar.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Ta bort vår anpassade stil från dokumentets stilsamling.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// All text som använde en borttagen stil återgår till standardformateringen.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
