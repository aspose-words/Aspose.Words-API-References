---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen AutomaticallyUpdate förbättrar dina stilar genom att automatiskt omdefiniera dem för optimalt värde och prestanda i dina projekt.
type: docs
weight: 20
url: /sv/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Anger om den här stilen automatiskt omdefinieras baserat på lämpligt värde.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Anmärkningar

Om egenskapsvärdet är inställt på sant omdefinierar MS Word automatiskt den aktuella stilen när lämplig styckeformatering har ändrats.

Egenskapen AutomaticallyUpdate gäller endast för styckeformat.

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

// Använd en av formaten från dokumentet på stycket som dokumentbyggaren skapar.
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
