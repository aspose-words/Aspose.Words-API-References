---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet Methode"
linktitle: "get_SavePictureBullet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet Methode. Wenn false, werden PictureBullet-Daten nicht im Ausgabedokument gespeichert. Der Standardwert ist true in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


Wenn **false**, werden PictureBullet‑Daten nicht im Ausgabedokument gespeichert. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Hinweise


Diese Option wird für Word 97 bereitgestellt, das nicht korrekt mit PictureBullet-Daten arbeiten kann. Um PictureBullet-Daten zu entfernen, setzen Sie die Option auf "false".

## Beispiele



Zeigt, wie PictureBullet-Daten beim Speichern aus dem Dokument weggelassen werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Einige Textverarbeitungsprogramme, wie Microsoft Word 97, sind mit PictureBullet-Daten inkompatibel.
// Durch das Setzen eines Flags im SaveOptions-Objekt,
// können wir beim Speichern alle Bild-Aufzählungszeichen in gewöhnliche Aufzählungszeichen umwandeln.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Siehe auch

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
