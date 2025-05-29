---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der SaveOptions ExportGeneratorName-Eigenschaft. Betten Sie den Namen und die Version von Aspose.Words ein, um die Rückverfolgbarkeit zu verbessern. Standardmäßig „true“.
type: docs
weight: 80
url: /de/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Beispiele

Zeigt, wie das Hinzufügen von Name und Version von Aspose.Words zu erstellten Dateien deaktiviert wird.

```csharp
Document doc = new Document();

// Verwenden Sie https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/, um zu erfahren, wie Sie das Ergebnis überprüfen können.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
