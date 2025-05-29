---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TxtLoadOptions för förbättrad inläsning av textdokument. Anpassa ditt dokumentobjekt med flexibla alternativ för optimal prestanda.
type: docs
weight: 4190
url: /sv/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Gör det möjligt att ange ytterligare alternativ vid laddningText dokument till ett[`Document`](../../aspose.words/document/) objekt.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Initierar en ny instans av den här klassen med standardvärden. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att antingen automatisk numreringsdetektering kommer att utföras när ett dokument laddas. Standardvärdet är`sann` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller anger om metafil ska konverteras(Wmf ellerEmf ) bilder tillPngbildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller anger om former ska konverteras med EquationXML till Office Math-objekt. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | Anger att antingen hyperlänkar i text ska detekteras. Standardvärdet är`falsk` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Gör det möjligt att ange hur numrerade listobjekt ska kännas igen när dokument importeras från oformaterat textformat. Standardvärdet är`sann`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Hämtar eller anger en dokumentriktning. Standardvärdet ärLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara`null` Standard är`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange dokumentets teckensnittsinställningar. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Anger om OLE-data ska ignoreras. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Hämtar eller ställer in önskat alternativ för hantering av inledande mellanrum. Standardvärdet ärConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet för det dokument som ska läsas in. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Gör det möjligt att ange att dokumentinläsningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Hämtar eller anger om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförloppet. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Tillåter användning av temporära filer vid läsning av dokument. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Hämtar eller ställer in önskat alternativ för hantering av efterföljande blanksteg. Standardvärdet ärTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Hämtar eller anger om LCID-värde från Windows-registret ska användas för att bestämma standardmarginaler för sidinställningar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Anropas under en inläsningsoperation, när ett problem upptäcks som kan leda till förlust av data- eller formateringsåtergivning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man läser och visar hyperlänkar.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Ladda dokument med hyperlänkar.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Skriv ut hyperlänkstext.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Se även

* class [LoadOptions](../loadoptions/)
* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
