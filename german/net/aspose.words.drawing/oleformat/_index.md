---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.OleFormat klas. Bietet Zugriff auf die Daten eines OLEObjekts oder ActiveXSteuerelements in C#.
type: docs
weight: 1150
url: /de/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Bietet Zugriff auf die Daten eines OLE-Objekts oder ActiveX-Steuerelements.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Ole-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OleFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Gibt an, ob der Link zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Ruft die CLSID des OLE-Objekts ab. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Ruft die Symbolbeschriftung des OLE-Objekts ab. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Gibt zurück`WAHR` ob das OLE-Objekt verknüpft ist (wann[`SourceFullName`](./sourcefullname/) angegeben ist). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Gibt an, ob der Link zum OLE-Objekt für Aktualisierungen gesperrt ist. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Ruft ab[`OleControl`](./olecontrol/) Objekte, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Ruft den Zeichenaspekt des OLE-Objekts ab. Wann`WAHR` , das OLE-Objekt wird als Symbol angezeigt. Wenn`FALSCH` , das OLE-Objekt wird als content. angezeigt |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Zugriff gewähren auf[`OlePackage`](../olepackage/) wenn das OLE-Objekt ein OLE-Paket ist. Gibt zurück`Null` sonst. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Ruft die ProgID des OLE-Objekts ab oder legt diese fest. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Ruft den Pfad und Namen der Quelldatei für das verknüpfte OLE-Objekt ab oder legt diesen fest. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Ruft eine Zeichenfolge ab oder legt diese fest, die zur Identifizierung des Teils der Quelldatei verwendet wird, der verknüpft wird. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Ruft die für das aktuell eingebettete Objekt vorgeschlagene Dateierweiterung ab, wenn Sie es in einer Datei speichern möchten. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Ruft den für das aktuell eingebettete Objekt vorgeschlagenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Ruft den OLE-Objektdateneintrag ab. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Ruft OLE-Objekt-Rohdaten ab. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Speichert die Daten des eingebetteten Objekts im angegebenen Stream. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen. |

## Bemerkungen

Benutzen Sie die[`OleFormat`](../shape/oleformat/)Eigenschaft, um auf die Daten eines OLE-Objekts zuzugreifen. Sie erstellen keine Instanzen davon`OleFormat` Klasse direkt.

## Beispiele

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Unser Objekt wird weder automatisch aktualisiert noch für Aktualisierungen gesperrt.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Wenn wir planen, das OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern,
// Wir können die Eigenschaft „SuggestedExtension“ verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nachfolgend finden Sie zwei Möglichkeiten, ein OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern.
// 1 - Über einen Stream speichern:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 – Direkt unter einem Dateinamen speichern:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
