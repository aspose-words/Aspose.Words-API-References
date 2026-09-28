---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles метод"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles метод. Когда значение false, небольшие метафайлы не сжимаются из соображений производительности. Значение по умолчанию — true, все метафайлы сжимаются независимо от их размера в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


Когда **false**, небольшие метафайлы не сжимаются по соображениям производительности. Значение по умолчанию — **true**, все метафайлы сжимаются независимо от их размера.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Примеры



Показывает, как изменить сжатие метафайлов в документе при сохранении.
```cpp
// Откройте документ, содержащий формулу Microsoft Equation 3.0.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// При сохранении документа небольшие метафайлы не сжимаются из соображений производительности.
// Мы можем установить флаг в объекте SaveOptions, чтобы сжимать каждый метафайл при сохранении.
// Некоторые редакторы, такие как LibreOffice, не могут читать несжатые метафайлы.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## См. также

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
