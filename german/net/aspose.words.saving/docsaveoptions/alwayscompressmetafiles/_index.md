---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Dokumentenmanagement mit der Eigenschaft „AlwaysCompressMetafiles“. Verbessern Sie die Leistung durch die Steuerung der Metadateikomprimierung für mehr Effizienz.
type: docs
weight: 20
url: /de/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Wann`FALSCH` , kleine Metadateien werden aus Leistungsgründen nicht komprimiert. Der Standardwert ist`WAHR` , alle Metadateien werden unabhängig von ihrer Größe komprimiert.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Beispiele

Zeigt, wie die Komprimierung von Metadateien in einem Dokument beim Speichern geändert wird.

```csharp
// Öffnen Sie ein Dokument, das eine Microsoft Equation 3.0-Formel enthält.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Wenn wir ein Dokument speichern, werden kleinere Metadateien aus Leistungsgründen nicht komprimiert.
// Wir können in einem SaveOptions-Objekt ein Flag setzen, um jede Metadatei beim Speichern zu komprimieren.
// Einige Editoren wie LibreOffice können unkomprimierte Metadateien nicht lesen.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Siehe auch

* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
