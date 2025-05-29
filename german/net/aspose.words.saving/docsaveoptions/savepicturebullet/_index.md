---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SavePictureBullet-Eigenschaft von DocSaveOptions Ihre Dokumentausgabe verbessert. Steuern Sie die PictureBullet-Datenspeicherung mühelos für optimale Ergebnisse.
type: docs
weight: 60
url: /de/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Wann`FALSCH` , PictureBullet-Daten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist`WAHR` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Bemerkungen

Diese Option ist für Word 97 vorgesehen, das mit PictureBullet-Daten nicht richtig arbeiten kann. Um PictureBullet-Daten zu entfernen, setzen Sie die Option auf „false“.

## Beispiele

Zeigt, wie PictureBullet-Daten beim Speichern aus dem Dokument weggelassen werden.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Einige Textverarbeitungsprogramme, wie beispielsweise Microsoft Word 97, sind mit PictureBullet-Daten nicht kompatibel.
// Durch Setzen eines Flags im SaveOptions-Objekt,
// Wir können alle Aufzählungspunkte des Bildes beim Speichern in normale Aufzählungspunkte umwandeln.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Siehe auch

* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
