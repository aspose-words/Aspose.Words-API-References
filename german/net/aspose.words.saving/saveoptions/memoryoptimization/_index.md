---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words für .NET
description: Verbessern Sie die Dokumentleistung mit der SaveOptions MemoryOptimization-Eigenschaft. Kontrollieren Sie die Speichernutzung vor dem Speichern und steigern Sie so Effizienz und Geschwindigkeit.
type: docs
weight: 100
url: /de/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Bemerkungen

Setzen dieser Option auf`WAHR` kann den Speicherverbrauch beim Speichern großer Dokumente erheblich senken, allerdings auf Kosten einer langsameren Speicherzeit.

## Beispiele

Zeigt eine Option zur Optimierung des Speicherverbrauchs beim Rendern großer Dokumente in PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „true“, um den Speicherbedarf beim Speichern großer Dokumente zu verringern
// auf Kosten einer Verlängerung der Operationsdauer.
// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „false“, um das Dokument normal als PDF zu speichern.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
