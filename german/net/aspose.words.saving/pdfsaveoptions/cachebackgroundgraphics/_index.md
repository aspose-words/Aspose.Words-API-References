---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words für .NET
description: Entdecken Sie die CacheBackgroundGraphics-Eigenschaft von PdfSaveOptions, um das Zwischenspeichern von Dokumentgrafiken zu optimieren und so Ihre PDF-Erstellung und -Leistung zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Hintergrund des Dokuments platzierte Grafiken zwischengespeichert werden sollen oder nicht.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` und Hintergrundgrafiken werden als xObject in das PDF-Dokument geschrieben.

Wenn der Wert`FALSCH` Hintergrundgrafiken werden nicht zwischengespeichert.

Für einige Formen wird das Zwischenspeichern nicht unterstützt (Formen mit Feldern, Lesezeichen, HRefs).

Bei der Dokumenthintergrundgrafik handelt es sich um verschiedene Formen, Diagramme und Bilder, die in der Fußzeile oder Kopfzeile sowie als Hintergrund und Rahmen einer Seite platziert werden.

## Beispiele

Zeigt, wie im Hintergrund eines Dokuments platzierte Grafiken zwischengespeichert werden.

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
