---
title: Style.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen ListFormat för styckeformat, vilket förbättrar dokumentets organisation och visuella attraktionskraft.
type: docs
weight: 110
url: /sv/net/aspose.words/style/listformat/
---
## Style.ListFormat property

Ger åtkomst till listformateringsegenskaperna för ett styckeformat.

```csharp
public ListFormat ListFormat { get; }
```

## Anmärkningar

Den här egenskapen är endast giltig för styckeformat. För andra formattyper returnerar den här egenskapen`null`.

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
