---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PclSaveOptions FallbackFontName“, die nahtloses Drucken mit einer Standardschriftart gewährleistet, wenn die gewünschte Schriftart nicht verfügbar ist.
type: docs
weight: 20
url: /de/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Name der Schriftart, die verwendet wird, wenn in den Drucker- und integrierten Schriftartensammlungen keine erwartete Schriftart gefunden wird.

```csharp
public string FallbackFontName { get; set; }
```

## Bemerkungen

Wenn kein Fallback gefunden wird, wird eine Warnung generiert und die Schriftart „Arial“ verwendet.

## Beispiele

Zeigt, wie eine Schriftart deklariert wird, die ein Drucker als Ersatz für gedruckten Text anwendet, wenn die Originalschriftart nicht verfügbar ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Dieses Dokument weist den Drucker an, „Times New Roman“ auf den Text mit der fehlenden Schriftart anzuwenden.
// Sollte auch „Times New Roman“ nicht verfügbar sein, druckt der Drucker standardmäßig die Schriftart „Arial“.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Siehe auch

* class [PclSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
