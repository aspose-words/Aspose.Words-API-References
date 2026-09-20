---
title: "метод Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes"
linktitle: "get_RenderNonImageShapes"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes. Получает или задает значение, указывающее, следует ли рендерить и записывать в выходной документ Docling JSON формы, не являющиеся изображениями, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Получает или задает значение, указывающее, должны ли не графические формы быть отрисованы и записаны в выходной JSON‑документ Docling.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
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

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
