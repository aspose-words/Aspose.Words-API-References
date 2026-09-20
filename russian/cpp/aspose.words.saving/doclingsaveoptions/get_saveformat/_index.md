---
title: "метод Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat. Указывает формат, в котором будет сохраняться документ, если используется этот объект параметров сохранения. Может быть только Docling в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохраняться документ, если используется этот объект параметров сохранения. Может быть только [Docling](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## Примеры



Показывает, как сохранить документ в формате Docling JSON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Установите значение true, чтобы отрисовать не графические формы и включить их в вывод.
// Установите значение false (по умолчанию), чтобы исключить не графические формы из вывода.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
