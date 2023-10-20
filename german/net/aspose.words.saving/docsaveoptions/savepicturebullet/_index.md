---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words für .NET
description: DocSaveOptions SavePictureBullet eigendom. WannFALSCH  PictureBulletDaten werden nicht im Ausgabedokument gespeichert. Der Standardwert istWAHR  in C#.
type: docs
weight: 50
url: /de/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Wann`FALSCH` , PictureBullet-Daten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist`WAHR` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Bemerkungen

Diese Option ist für Word 97 verfügbar, das mit PictureBullet-Daten nicht ordnungsgemäß funktionieren kann. Um PictureBullet-Daten zu entfernen, setzen Sie die Option auf „false“.

## Beispiele

Zeigt, wie PictureBullet-Daten beim Speichern aus dem Dokument weggelassen werden.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Einige Textverarbeitungsprogramme wie Microsoft Word 97 sind nicht mit PictureBullet-Daten kompatibel.
// Durch Setzen eines Flags im SaveOptions-Objekt,
// Wir können beim Speichern alle Bildaufzählungspunkte in normale Aufzählungspunkte umwandeln.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Siehe auch

* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
