---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.OleFormat für den nahtlosen Zugriff auf OLE-Objekte und ActiveX-Steuerelemente und verbessern Sie so Ihre Dokumentverarbeitungsfunktionen.
type: docs
weight: 1530
url: /de/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Bietet Zugriff auf die Daten eines OLE-Objekts oder ActiveX-Steuerelements.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit OLE-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OleFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Gibt an, ob die Verknüpfung zum OLE-Objekt in Microsoft Word automatisch aktualisiert wird oder nicht. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Ruft die CLSID des OLE-Objekts ab. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Ruft die Symbolbeschriftung des OLE-Objekts ab. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Rückgaben`WAHR` wenn das OLE-Objekt verknüpft ist (wenn[`SourceFullName`](./sourcefullname/) angegeben ist). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Gibt an, ob die Verknüpfung zum OLE-Objekt vor Aktualisierungen gesperrt ist. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Ruft ab[`OleControl`](./olecontrol/) Objekte, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Ruft den Zeichenaspekt des OLE-Objekts ab. Wenn`WAHR`wird das OLE-Objekt als Symbol angezeigt. Wenn`FALSCH` , das OLE-Objekt wird als Inhalt angezeigt. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Zugriff gewähren auf[`OlePackage`](../olepackage/) wenn das OLE-Objekt ein OLE-Paket ist. Gibt zurück`null` andernfalls. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Ruft die ProgID des OLE-Objekts ab oder legt sie fest. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Ruft den Pfad und den Namen der Quelldatei für das verknüpfte OLE-Objekt ab oder legt diese fest. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die zum Identifizieren des Teils der Quelldatei verwendet wird, der verknüpft wird. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Ruft die für das aktuelle eingebettete Objekt vorgeschlagene Dateierweiterung ab, wenn Sie es in einer Datei speichern möchten. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Ruft den für das aktuelle eingebettete Objekt vorgeschlagenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Ruft den Dateneintrag des OLE-Objekts ab. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Ruft Rohdaten des OLE-Objekts ab. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Speichert die Daten des eingebetteten Objekts im angegebenen Stream. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Speichert die Daten des eingebetteten Objekts in einer Datei mit dem angegebenen Namen. |

## Bemerkungen

Verwenden Sie die[`OleFormat`](../shape/oleformat/) Eigenschaft, um auf die Daten eines OLE-Objekts zuzugreifen. Sie erstellen keine Instanzen der`OleFormat` Klasse direkt.

## Beispiele

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Unser Objekt wird weder automatisch aktualisiert noch ist es für Aktualisierungen gesperrt.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Wenn wir das OLE-Objekt in einer Datei im lokalen Dateisystem speichern möchten,
// Wir können die Eigenschaft „SuggestedExtension“ verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Unten sind zwei Möglichkeiten zum Speichern eines OLE-Objekts in einer Datei im lokalen Dateisystem aufgeführt.
// 1 - Speichern Sie es über einen Stream:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Speichern Sie es direkt unter einem Dateinamen:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
