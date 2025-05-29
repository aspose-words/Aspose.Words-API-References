---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words für .NET
description: Führen Sie mit der Methode „MergeToImages“ mühelos mehrere Dokumente zusammen, erstellen Sie eine einzelne Bildausgabe und passen Sie dabei Dateinamen und Speicheroptionen an.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Fügt die angegebenen Eingabedokumente unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und Speicheroptionen zu einem einzigen Ausgabedokument zusammen. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | String[] | Die Namen der Eingabedateien. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Fügt die angegebenen Eingabedokumentströme unter Verwendung der angegebenen Bildspeicheroptionen zu einem einzigen Ausgabedokument zusammen. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | Stream[] | Die Eingabedatei wird gestreamt. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| mergeFormatMode | MergeFormatMode | Gibt an, wie kollidierende Formatierungen zusammengeführt werden. |

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
