---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words für .NET
description: Aspose.Words.Rendering.AsposeWordsPrintDocument klas. Stellt eine Standardimplementierung zum Drucken von a bereitDocument innerhalb des .NETDruckframeworks in C#.
type: docs
weight: 4530
url: /de/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Stellt eine Standardimplementierung zum Drucken von a bereit[`Document`](../../aspose.words/document/) innerhalb des .NET-Druckframeworks.

Um mehr zu erfahren, besuchen Sie die[Drucken eines Dokuments programmgesteuert oder mithilfe von Dialogen](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) Dokumentationsartikel.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Ruft ab oder legt fest, wie nicht farbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Ruft die Anzahl der in Farbe gedruckten Seiten ab (d. h. mitColor auf true setzen). |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Liest und speichert einige Felder vonPrinterSettings zur Reduzierung der Druckzeit. |

## Bemerkungen

`AsposeWordsPrintDocument` überschreibtPrintEventArgs) zum Drucken des in angegebenen SeitenbereichsPrinterSettings.

Ein einzelnes Word-Dokument kann aus mehreren Abschnitten bestehen, die Seiten mit unterschiedlichen Größen, Ausrichtungen und Papierfächern angeben.`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) um Papierformat, Ausrichtung und Papierquelle beim Drucken eines Word-Dokuments richtig auszuwählen.

Microsoft Word speichert druckerspezifische Werte für Papierfächer in einem Word-Dokument und daher führt nur das Drucken auf demselben Druckermodell wie dem, das ausgewählt wurde, als der Benutzer die Papierfächer angegeben hat, zum Drucken aus den richtigen Fächern. Wenn Sie ein Dokument auf einem anderen Drucker drucken, wird höchstwahrscheinlich das Standardpapierfach verwendet und nicht die im Dokument angegebenen Fächer.

### Siehe auch

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
