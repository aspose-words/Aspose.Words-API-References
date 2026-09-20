---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet метод"
linktitle: "get_SavePictureBullet"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet метод. Когда значение ложно, данные PictureBullet не сохраняются в выходной документ. Значение по умолчанию — истинно в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


Когда **false**, данные PictureBullet не сохраняются в выходной документ. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Примечания


Эта опция предоставлена для Word 97, который не может корректно работать с данными PictureBullet. Чтобы удалить данные PictureBullet, установите опцию в значение "false".

## Примеры



Показывает, как исключить данные PictureBullet из документа при сохранении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Некоторые текстовые процессоры, такие как Microsoft Word 97, несовместимы с данными PictureBullet.
// Установив флаг в объекте SaveOptions,
// мы можем преобразовать все пункты‑маркировки изображениями в обычные пункты‑маркировки при сохранении.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## См. также

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
