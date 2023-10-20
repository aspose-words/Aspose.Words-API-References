---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words für .NET
description: Aspose.Words.ImportFormatMode opsomming. Gibt an wie die Formatierung beim Importieren von Inhalten aus einem anderen Dokument zusammengeführt wird in C#.
type: docs
weight: 3230
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
| UseDestinationStyles | `0` | Verwenden Sie die Stile des Zieldokuments und kopieren Sie neue Stile. Dies ist die Standardoption. |
| KeepSourceFormatting | `1` | Kopieren Sie alle erforderlichen Stile in das Zieldokument und generieren Sie bei Bedarf eindeutige Stilnamen. |
| KeepDifferentStyles | `2` | Kopieren Sie nur Stile, die sich von denen im Quelldokument unterscheiden. |

## Bemerkungen

Wenn Sie Knoten von einem Dokument in ein anderes kopieren, gibt diese Option an, wie formatting aufgelöst wird, wenn beide Dokumente einen Stil mit demselben Namen, aber unterschiedlicher Formatierung haben.

Die Formatierung wird wie folgt aufgelöst:

1. Integrierte Stile werden anhand ihrer ortsunabhängigen Stilkennung abgeglichen. Benutzerdefinierte Stile werden anhand des Stilnamens unter Berücksichtigung der Groß-/Kleinschreibung abgeglichen.
2. Wenn im Zieldokument kein passender Stil gefunden wird, werden style (und alle darin referenzierten Stile) in das Ziel document kopiert und die importierten Knoten werden aktualisiert, um auf den neuen Stil zu verweisen.
3. Wenn im Zieldokument bereits ein passender Stil vorhanden ist, hängt das, was passiert , davon ab`importFormatMode` Parameter übergeben an [`Document.ImportNode`](../documentbase/importnode/) wie unten beschrieben.

Bei Verwendung desUseDestinationStyles Option: Wenn bereits ein passender Stil im Zieldokument vorhanden ist, wird der Stil nicht kopiert und die importierten Knoten werden aktualisiert , um auf den vorhandenen Stil zu verweisen.

Der Nachteil der VerwendungUseDestinationStylesist, dass der importierte Text im Zieldokument möglicherweise anders aussieht als im Quelldokument. Beispielsweise verwendet der Stil „Überschrift 1“ im Quelldokument die Schriftart Arial 16pt und der Stil „Überschrift 1“ im Zieldokument Times New Schriftart Roman 14pt. Beim Importieren von Text im Stil „Überschrift 1“ ohne andere direkte Formatierung wird dieser im Zieldokument als Schriftart Times New Roman 14pt angezeigt.

KeepSourceFormattingMit dieser Option können Sie sicherstellen, dass der importierte Inhalt im Zieldokument genauso aussieht wie im Quelldokument. Wenn im Zieldokument bereits ein passender Stil vorhanden ist, wird die Formatierung des Quellstils in direkte Knotenattribute erweitert und der Stil wird erweitert in „Normal“ geändert. Wenn der Stil im Zieldokument nicht vorhanden ist, wird der Quellstil in das Zieldokument importiert und auf den importierten Knoten angewendet. Beachten Sie, dass es nicht immer möglich ist, den Quellstil beizubehalten, selbst wenn er vorhanden ist ist im Zieldokument nicht vorhanden. In diesem Fall wird die Formatierung eines solchen Stils in direkte Node-Attribute erweitert, um die ursprüngliche Node-Formatierung beizubehalten.

Der Nachteil der VerwendungKeepSourceFormattingWenn Sie mehrere Importe durchführen, könnten im Zieldokument viele Stile vorhanden sein, was die Verwendung einer konsistenten Stilformatierung in Microsoft Word für dieses Dokument erschweren könnte.

BenutzenKeepDifferentStyles Option ermöglicht die Wiederverwendung von Zielstilen , wenn die von ihnen bereitgestellte Formatierung mit den Stilen im Quelldokument identisch ist. Wenn sich der Stil im Zieldokument von der Quelle unterscheidet, wird er importiert.

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
