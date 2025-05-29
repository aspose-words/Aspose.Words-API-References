---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.ImportFormatMode die Dokumentformatierung verbessert, indem es Stile aus importierten Inhalten nahtlos zusammenführt, um optimale Ergebnisse zu erzielen.
type: docs
weight: 3680
url: /de/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Gibt an, wie die Formatierung beim Importieren von Inhalten aus einem anderen Dokument zusammengeführt wird.

```csharp
public enum ImportFormatMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseDestinationStyles | `0` | Die Formatvorlagen des Zieldokuments verwenden und neue Formatvorlagen kopieren. Dies ist die Standardoption. |
| KeepSourceFormatting | `1` | Kopieren Sie alle erforderlichen Stile in das Zieldokument und generieren Sie bei Bedarf eindeutige Stilnamen. |
| KeepDifferentStyles | `2` | Kopieren Sie nur Stile, die sich von denen im Quelldokument unterscheiden. |

## Bemerkungen

Wenn Sie Knoten von einem Dokument in ein anderes kopieren, gibt diese Option an, wie formatting aufgelöst wird, wenn beide Dokumente einen Stil mit demselben Namen, aber unterschiedlicher Formatierung haben.

Die Formatierung wird wie folgt aufgelöst:

1. Integrierte Stile werden anhand ihrer gebietsschemaunabhängigen Stilkennung abgeglichen. Benutzerdefinierte Stile werden anhand eines Stilnamens abgeglichen, bei dem die Groß-/Kleinschreibung beachtet wird.
2. Wenn im Zieldokument kein passender Stil gefunden wird, wird der Stil (und alle darin referenzierten Stile) in das Zieldokument kopiert und die importierten Knoten werden aktualisiert, um auf den neuen Stil zu verweisen.
3. Wenn im Zieldokument bereits ein passender Stil vorhanden ist, hängt das Geschehen von der`Importformatmodus` Parameter übergeben an [`ImportNode`](../documentbase/importnode/) wie unten beschrieben.

Bei Verwendung desUseDestinationStyles Wenn im Zieldokument bereits ein passender Stil vorhanden ist , wird der Stil nicht kopiert und die importierten Knoten werden aktualisiert , um auf den vorhandenen Stil zu verweisen.

Der Nachteil der VerwendungUseDestinationStylesbesteht darin, dass der importierte Text im Zieldokument möglicherweise anders aussieht als im Quelldokument. Beispielsweise verwendet der Stil „Überschrift 1“ im Quelldokument die Schriftart Arial 16pt und der Stil „Überschrift 1“ im Zieldokument die Schriftart Times New Roman 14pt. Wenn Sie Text im Stil „Überschrift 1“ ohne andere direkte Formatierung importieren, wird er im Zieldokument in der Schriftart Times New Roman 14pt angezeigt.

KeepSourceFormattingMit dieser Option können Sie sicherstellen, dass der importierte Inhalt im Zieldokument genauso aussieht wie im Quelldokument. Wenn im Zieldokument bereits ein passender Stil vorhanden ist, wird die Formatierung des Quellstils in direkte Knotenattribute erweitert und der Stil in „Normal“ geändert. Wenn der Stil im Zieldokument nicht vorhanden ist, wird der Quellstil in das Zieldokument importiert und auf den importierten Knoten angewendet. Beachten Sie, dass es nicht immer möglich ist, den Quellstil beizubehalten, selbst wenn er im Zieldokument nicht vorhanden ist. In diesem Fall wird die Formatierung eines solchen Stils in direkte Knotenattribute erweitert, anstatt die ursprüngliche Knotenformatierung beizubehalten.

Der Nachteil der VerwendungKeepSourceFormattingWenn Sie mehrere Importe durchführen, kann es passieren, dass das Zieldokument viele Stile enthält, was die Verwendung einer konsistenten Stilformatierung in Microsoft Word für dieses Dokument erschweren könnte.

VerwendenKeepDifferentStyles Die Option ermöglicht die Wiederverwendung von Zielstilen , wenn die von ihnen bereitgestellte Formatierung mit den Stilen im Quelldokument identisch ist. Wenn sich der Stil im Zieldokument von dem der Quelle unterscheidet, wird er importiert.

## Beispiele

Zeigt, wie ein Dokument in ein anderes Dokument eingefügt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
