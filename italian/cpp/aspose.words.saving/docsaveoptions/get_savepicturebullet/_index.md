---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method"
linktitle: "get_SavePictureBullet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method. Quando è false, i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito è true in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


Quando **false**, i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Note


Questa opzione è fornita per Word 97, che non può gestire correttamente i dati PictureBullet. Per rimuovere i dati PictureBullet, impostare l'opzione su "false".

## Esempi



Mostra come omettere i dati PictureBullet dal documento durante il salvataggio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Alcuni elaboratori di testi, come Microsoft Word 97, sono incompatibili con i dati PictureBullet.
// Impostando un flag nell'oggetto SaveOptions,
// possiamo convertire tutti i punti elenco immagine in punti elenco ordinari durante il salvataggio.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Vedi anche

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
