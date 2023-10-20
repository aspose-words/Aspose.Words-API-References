---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words für .NET
description: SaveOptions ExportGeneratorName eigendom. WannWAHR  bewirkt dass der Name und die Version von Aspose.Words in erzeugte Dateien eingebettet werden. Der Standardwert istWAHR  in C#.
type: docs
weight: 80
url: /de/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in erzeugte Dateien eingebettet werden. Der Standardwert ist`WAHR` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Beispiele

Zeigt, wie das Hinzufügen von Namen und Version von Aspose.Words zu erzeugten Dateien deaktiviert wird.

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
