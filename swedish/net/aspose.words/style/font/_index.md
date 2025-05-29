---
title: Style.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Stil Teckensnitt för att enkelt förbättra din teckenformatering. Lås upp unika stilalternativ för ett elegant utseende!
type: docs
weight: 60
url: /sv/net/aspose.words/style/font/
---
## Style.Font property

Hämtar teckenformateringen för stilen.

```csharp
public Font Font { get; }
```

## Anmärkningar

För listformat returnerar den här egenskapen`null`.

## Exempel

Visar hur man skapar och använder ett styckeformat med listformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett anpassat styckeformat.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Skapa en lista och se till att stycken som använder den här stilen kommer att använda den här listan.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Använd styckeformatet på dokumentbyggarens aktuella stycke och lägg sedan till lite text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändra dokumentbyggarens stil till en som inte har någon listformatering och skriv ett annat stycke.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

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

* class [Font](../../font/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
