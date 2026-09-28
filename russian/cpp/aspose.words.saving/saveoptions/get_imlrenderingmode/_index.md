---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode метод"
linktitle: "get_ImlRenderingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode метод. Получает или задаёт значение, определяющее, как отображаются объекты чернил (InkML) в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Получает или задает значение, определяющее, как отображаются объекты чернил (InkML).

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Примечания


Значение по умолчанию — [InkML](../../imlrenderingmode/).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

## Примеры



Показывает, как отрисовать объект Ink.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Установите 'ImlRenderingMode.InkML', который игнорирует резервную форму объекта чернил (InkML) и рендерит сам InkML.
// Если результат рендеринга неудовлетворителен,
// пожалуйста, используйте 'ImlRenderingMode.Fallback', чтобы получить результат, похожий на предыдущие версии.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## См. также

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
