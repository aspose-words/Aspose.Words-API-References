---
title: Style
second_title: Aspose.Words för .NET API Referens
description: Representerar en enda inbyggd eller användardefinierad stil.
type: docs
weight: 5830
url: /sv/net/aspose.words/style/
---
## Style class

Representerar en enda inbyggd eller användardefinierad stil.

```csharp
public class Style
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases) { get; } | Får alla alias för denna stil. Om stilen inte har några alias returneras tom array av sträng. |
| [BaseStyleName](../../aspose.words/style/basestylename) { get; set; } | Hämtar/ställer in namnet på stilen som denna stil är baserad på. |
| [BuiltIn](../../aspose.words/style/builtin) { get; } | Sant om denna stil är en av de inbyggda stilarna i MS Word. |
| [Document](../../aspose.words/style/document) { get; } | Hämtar ägardokumentet. |
| [Font](../../aspose.words/style/font) { get; } | Hämtar teckenformateringen för stilen. |
| [IsHeading](../../aspose.words/style/isheading) { get; } | Sant när stilen är en av de inbyggda rubrikstilarna. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle) { get; set; } | Anger om denna stil visas i Quick Style-galleriet i MS Word UI. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename) { get; } | Hämtar namnet på stilen som är länkad till denna. Returnerar tom sträng om inga stilar är länkade. |
| [List](../../aspose.words/style/list) { get; } | Hämtar listan som definierar formateringen av denna liststil. |
| [ListFormat](../../aspose.words/style/listformat) { get; } | Ger tillgång till listformateringsegenskaperna för en styckestil. |
| [Name](../../aspose.words/style/name) { get; set; } | Hämtar eller ställer in namnet på stilen. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename) { get; set; } | Hämtar/ställer in namnet på formatet som ska tillämpas automatiskt på ett nytt stycke som infogas efter a stycke formaterat med det angivna formatet. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat) { get; } | Hämtar formatets styckeformatering. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier) { get; } | Hämtar den lokala stilidentifieraren för en inbyggd stil. |
| [Styles](../../aspose.words/style/styles) { get; } | Får samlingen av stilar som denna stil tillhör. |
| [Type](../../aspose.words/style/type) { get; } | Hämtar stiltypen (stycke eller tecken). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Equals](../../aspose.words/style/equals#equals)(Style) | Jämförs med den angivna stilen. Stilar Istds jämförs endast för inbyggda stilar. Formatmallars standarder ingår inte i jämförelsen. Basstil, länkad stil och nästa styckestil jämförs rekursivt. |
| [Remove](../../aspose.words/style/remove)() | Tar bort den angivna stilen från dokumentet. |

### Exempel

Visar hur du skapar och använder ett styckeformat med listformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en anpassad styckestil.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Skapa en lista och se till att styckena som använder den här stilen kommer att använda den här listan.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Använd styckeformatet på dokumentbyggarens nuvarande stycke och lägg sedan till lite text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändra dokumentbyggarens stil till en som inte har någon listformatering och skriv ett stycke till.
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

* namnutrymme [Aspose.Words](../../aspose.words)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
