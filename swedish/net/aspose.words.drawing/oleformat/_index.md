---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.OleFormat för sömlös åtkomst till OLE-objekt och ActiveX-kontroller, vilket förbättrar dina dokumentbehandlingsmöjligheter.
type: docs
weight: 1530
url: /sv/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Ger åtkomst till data i ett OLE-objekt eller en ActiveX-kontroll.

För att lära dig mer, besök[Arbeta med Ole-objekt](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public class OleFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Anger om länken till OLE-objektet uppdateras automatiskt eller inte i Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Hämtar CLSID för OLE-objektet. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Hämtar ikontext för OLE-objekt. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Returer`sann` om OLE-objektet är länkat (när[`SourceFullName`](./sourcefullname/) är specificerad). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Anger om länken till OLE-objektet är låst från uppdateringar. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Får[`OleControl`](./olecontrol/) objekt om detta OLE-objekt är en ActiveX-kontroll. Annars är egenskapen null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Hämtar ritningsaspekten av OLE-objektet. När`sann` visas OLE-objektet som en ikon. När`falsk` , OLE-objektet visas som innehåll. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Ge åtkomst till[`OlePackage`](../olepackage/) om OLE-objektet är ett OLE-paket. Returnerar`null` annars. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Hämtar eller anger ProgID för OLE-objektet. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Hämtar eller anger sökvägen och namnet på källfilen för det länkade OLE-objektet. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Hämtar eller anger en sträng som används för att identifiera den del av källfilen som länkas. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Hämtar den föreslagna filändelsen för det aktuella inbäddade objektet om du vill spara det i en fil. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Hämtar det föreslagna filnamnet för det aktuella inbäddade objektet om du vill spara det i en fil. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Hämtar datainmatning för OLE-objekt. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Hämtar rådata för OLE-objekt. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Sparar data från det inbäddade objektet i den angivna strömmen. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Sparar data från det inbäddade objektet i en fil med det angivna namnet. |

## Anmärkningar

Använd[`OleFormat`](../shape/oleformat/) egenskapen för att komma åt data i ett OLE-objekt. Du skapar inte instanser av`OleFormat` klass direkt.

## Exempel

Visar hur man extraherar inbäddade OLE-objekt till filer.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Vårt mål är varken automatisk uppdatering eller låst från uppdateringar.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// vi kan använda egenskapen "SuggestedExtension" för att avgöra vilket filtillägg som ska tillämpas på filen.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nedan följer två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 - Spara det via en ström:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Spara det direkt till ett filnamn:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
