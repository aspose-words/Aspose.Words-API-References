---
title: DocSaveOptions.SavePictureBullet
second_title: Aspose.Words für .NET-API-Referenz
description: DocSaveOptions eigendom. WannFALSCH  PictureBulletDaten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist Stimmt .
type: docs
weight: 50
url: /de/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Wann`FALSCH` , PictureBullet-Daten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist **Stimmt** .

```csharp
public bool SavePictureBullet { get; set; }
```

### Bemerkungen

Diese Option wird für Word 97 bereitgestellt, das mit PictureBullet-Daten nicht richtig arbeiten kann. Um PictureBullet-Daten zu entfernen, setzen Sie die Option auf „false“.

### Beispiele

Zeigt, wie PictureBullet-Daten beim Speichern aus dem Dokument weggelassen werden.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");

// Einige Textverarbeitungsprogramme wie Microsoft Word 97 sind mit PictureBullet-Daten nicht kompatibel.
// Durch Setzen eines Flags im SaveOptions-Objekt,
// Wir können beim Speichern alle Bildaufzählungspunkte in gewöhnliche Aufzählungspunkte umwandeln.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Siehe auch

* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../docsaveoptions/)
* Montage [Aspose.Words](../../../)


