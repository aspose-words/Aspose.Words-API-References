---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ImportFormatOptions för anpassningsbar dokumentformatering. Förbättra dina utskrifter med skräddarsydda importinställningar för optimala resultat.
type: docs
weight: 3690
url: /sv/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Gör det möjligt att ange olika importalternativ för att formatera utdata.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

```csharp
public class ImportFormatOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om avståndet mellan meningar och ord ska justeras automatiskt. Standardvärdet är`falsk` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Hämtar eller anger ett booleskt värde som anger att antingen motstridiga stilar ska kopieras inKeepSourceFormatting läge. Standardvärdet är`falsk` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att källformateringen av innehållet i sidhuvuden/sidfoten ignoreras. omKeepSourceFormatting läget används. Standardvärdet är`sann` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att källformateringen av textrutes innehåll ignoreras omKeepSourceFormatting läget används. Standardvärdet är`sann` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger hur numreringen ska importeras när den kolliderar i käll- och destinationsdokument. Standardvärdet är`falsk` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inklistrade listor ska slås samman med omgivande listor. Standardvärdet är`falsk` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger hur stilar importeras när de har samma namn i käll- och destinationsdokument. Standardvärdet är`falsk` . |

## Exempel

Visar hur man åtgärdar dubbletter av format när man infogar dokument.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil så att den har en annan färg än originalets.
// Om vi infogar klonen i originaldokumentet kommer de två stilarna med samma namn att orsaka en kollision.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words löser stilkrockar genom att konvertera källdokumentets stilar.
// med samma namn som destinationsformat till direkta styckeattribut.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
