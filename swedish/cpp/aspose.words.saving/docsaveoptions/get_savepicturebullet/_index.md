---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet metod"
linktitle: "get_SavePictureBullet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet metod. När false sparas inte PictureBullet-data till utdata-dokumentet. Standardvärdet är true i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


När **false** sparas inte PictureBullet‑data till utdata‑dokumentet. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Anmärkningar


Detta alternativ tillhandahålls för Word 97, som inte kan fungera korrekt med PictureBullet-data. För att ta bort PictureBullet-data, sätt alternativet till "false".

## Exempel



Visar hur man utelämnar PictureBullet-data från dokumentet vid sparande.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Vissa ordbehandlare, såsom Microsoft Word 97, är inkompatibla med PictureBullet-data.
// Genom att sätta en flagga i SaveOptions-objektet,
// kan vi konvertera alla bildpunkter till vanliga punkter vid sparande.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Se även

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
