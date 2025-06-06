---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.StyleCollection, som har en mängd olika inbyggda och anpassade stilobjekt för att förbättra dokumentets formatering och design.
type: docs
weight: 6990
url: /sv/net/aspose.words/stylecollection/
---
## StyleCollection class

En samling av[`Style`](../style/)objekt som representerar både de inbyggda och användardefinierade formaten i ett dokument.

För att lära dig mer, besök[Arbeta med stilar och teman](https://docs.aspose.com/words/net/working-with-styles-and-themes/) dokumentationsartikel.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Hämtar antalet stilar i kollektionen. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Hämtar standardtextformatering för dokumentet. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Hämtar standardformatering för stycke i dokumentet. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Hämtar ägardokumentet. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Hämtar en stil efter namn eller alias. (3 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Skapar en ny användardefinierad stil och lägger till den i samlingen. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Kopierar en stil till den här samlingen. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Tar bort alla stilar från panelen Snabbstilsgalleri. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Hämtar ett uppräknarobjekt som räknar upp stilar i alfabetisk ordning efter deras namn. |

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

* class [Style](../style/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
