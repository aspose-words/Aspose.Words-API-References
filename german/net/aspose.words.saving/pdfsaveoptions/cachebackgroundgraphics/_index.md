---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words für .NET
description: PdfSaveOptions CacheBackgroundGraphics eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt ob im Hintergrund des Dokuments platzierte Grafiken zwischengespeichert werden sollen oder nicht in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob im Hintergrund des Dokuments platzierte Grafiken zwischengespeichert werden sollen oder nicht.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` und Hintergrundgrafiken werden als xObject in das PDF-Dokument geschrieben.

Wenn der Wert ist`FALSCH` Hintergrundgrafiken werden nicht zwischengespeichert.

Einige Formen werden beim Caching nicht unterstützt (Formen mit Feldern, Lesezeichen, HRefs).

Bei der Hintergrundgrafik eines Dokuments handelt es sich um verschiedene Formen, Diagramme, Bilder, die in der Fuß- oder Kopfzeile platziert werden, sowie als Hintergrund und Rand einer Seite.

## Beispiele

Zeigt, wie im Hintergrund des Dokuments platzierte Grafiken zwischengespeichert werden.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
