---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Drawing.OlePackage för att enkelt hantera OLE Package-egenskaper och förbättra dina dokumentbehandlingsmöjligheter.
type: docs
weight: 1540
url: /sv/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Tillåter åtkomst till OLE-paketegenskaper.

För att lära dig mer, besök[Arbeta med Ole-objekt](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public class OlePackage
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Hämtar eller anger visningsnamn för OLE-paket. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Hämtar eller anger OLE-paketets filnamn. |

## Anmärkningar

OLE-paketet är ett äldre och "odokumenterat" sätt att lagra inbäddade objekt om OLE-hanteraren är okänd. Tidiga Windows-versioner som Windows 3.1, 95 och 98 hade Packager.exe-applikationen som kunde användas för att bädda in alla typer av data i dokument. Nu är den här applikationen exkluderad från Windows, men MS Word och andra program använder den fortfarande för att bädda in data om OLE-hanteraren saknas eller är okänd.

## Exempel

Visar hur man infogar ett OLE-objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE-objekt låter oss öppna andra filer i det lokala filsystemet med hjälp av ett annat installerat program
// i vårt operativsystem genom att dubbelklicka på formen som innehåller OLE-objektet i dokumentets brödtext.
// I det här fallet kommer vår externa fil att vara ett ZIP-arkiv.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
