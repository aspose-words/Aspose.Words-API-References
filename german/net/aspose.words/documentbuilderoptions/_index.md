---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.DocumentBuilderOptions, um Ihre Dokumenterstellung mit anpassbaren Funktionen für ein nahtloses Erstellungserlebnis zu verbessern.
type: docs
weight: 670
url: /de/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Ermöglicht die Angabe zusätzlicher Optionen für den Dokumenterstellungsprozess.

```csharp
public class DocumentBuilderOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Wahr, wenn die auf den Tabelleninhalt angewendete Formatierung keinen Einfluss auf die Formatierung des darauf folgenden Inhalts hat. Der Standardwert ist`WAHR` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Entspricht dem Entwurfsmodus in Microsoft Word. |

## Beispiele

Zeigt, wie die Tabellenformatierung für den Inhalt danach ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Fügt Inhalt vor der Tabelle hinzu.
// Die Standardschriftgröße ist 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Ändert die Schriftgröße innerhalb der Tabelle.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Wenn ContextTableFormatting wahr ist, wird die Tabellenformatierung anschließend nicht auf den Inhalt angewendet.
// Wenn ContextTableFormatting falsch ist, wird die Tabellenformatierung anschließend auf den Inhalt angewendet.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
