---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words för .NET
description: Upptäck hur du får tillgång till och anpassar styckeformateringen i stilar för förbättrad dokumentpresentation och professionell formatering.
type: docs
weight: 150
url: /sv/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Hämtar styckeformateringen för stilen.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Anmärkningar

För tecken- och listformat returnerar den här egenskapen`null`.

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

### Se även

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
