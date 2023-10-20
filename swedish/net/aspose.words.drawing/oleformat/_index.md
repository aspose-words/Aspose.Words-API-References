---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.OleFormat klass. Ger åtkomst till data för ett OLEobjekt eller ActiveXkontroll i C#.
type: docs
weight: 1150
url: /sv/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Ger åtkomst till data för ett OLE-objekt eller ActiveX-kontroll.

För att lära dig mer, besök[Arbeta med Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public class OleFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Anger om länken till OLE-objektet uppdateras automatiskt eller inte i Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Hämtar CLSID för OLE-objektet. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Får ikontext för OLE-objekt. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Returnerar`Sann` om OLE-objektet är länkat (när[`SourceFullName`](./sourcefullname/) anges). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Anger om länken till OLE-objektet är låst från uppdateringar. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Blir[`OleControl`](./olecontrol/) objekt om detta OLE-objekt är en ActiveX-kontroll. Annars är den här egenskapen null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Hämtar ritaspekten för OLE-objektet. När`Sann` , visas OLE-objektet som en ikon. When`falsk` , visas OLE-objektet som innehåll. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Ge åtkomst till[`OlePackage`](../olepackage/) om OLE-objekt är ett OLE Package. Returnerar`null` annars. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Hämtar eller ställer in ProgID för OLE-objektet. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Hämtar eller ställer in sökvägen och namnet på källfilen för det länkade OLE-objektet. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Hämtar eller ställer in en sträng som används för att identifiera den del av källfilen som länkas. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Hämtar filtillägget som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Hämtar filnamnet som föreslås för det aktuella inbäddade objektet om du vill spara det i en fil. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Hämtar OLE-objektdatainmatning. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Hämtar rådata för OLE-objekt. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Sparar data för det inbäddade objektet i den angivna strömmen. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Sparar data för det inbäddade objektet i en fil med det angivna namnet. |

## Anmärkningar

Använd[`OleFormat`](../shape/oleformat/)egenskap för att komma åt data för ett OLE-objekt. Du skapar inte instanser av`OleFormat` klass direkt.

## Exempel

Visar hur man extraherar inbäddade OLE-objekt till filer.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Vårt objekt är varken automatisk uppdatering eller låst från uppdateringar.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// vi kan använda egenskapen "SuggestedExtension" för att avgöra vilket filtillägg som ska tillämpas på filen.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nedan finns två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 - Spara det via en stream:
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
