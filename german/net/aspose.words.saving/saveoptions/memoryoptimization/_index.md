---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words für .NET
description: SaveOptions MemoryOptimization eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft istFALSCH  in C#.
type: docs
weight: 100
url: /de/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Bemerkungen

Diese Option festlegen auf`WAHR` kann den Speicherverbrauch erheblich senken und gleichzeitig große Dokumente speichern, allerdings auf Kosten einer langsameren Zeitersparnis.

## Beispiele

Zeigt eine Option zur Optimierung des Speicherverbrauchs beim Rendern großer Dokumente in PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „true“, um den Speicherbedarf bei Speichervorgängen großer Dokumente zu verringern
// auf Kosten einer Verlängerung der Operationsdauer.
// Setzen Sie die Eigenschaft „MemoryOptimization“ auf „false“, um das Dokument normal als PDF zu speichern.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
