---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie die ContextTableFormatting-Eigenschaft in DocumentBuilderOptions. Stellen Sie sicher, dass die Tabellenformatierung unabhängig bleibt, und verbessern Sie so die Übersichtlichkeit und den Stil Ihres Dokuments.
type: docs
weight: 20
url: /de/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Wahr, wenn die auf den Tabelleninhalt angewendete Formatierung keinen Einfluss auf die Formatierung des darauf folgenden Inhalts hat. Der Standardwert ist`WAHR` .

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
