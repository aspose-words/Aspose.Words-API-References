---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Указывает, как объекты чернил (InkML) отображаются в фиксированные форматы страниц в C++."
type: docs
weight: 66000
url: /ru/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Указывает, как объекты чернил (InkML) отображаются в фиксированные форматы страниц.

```cpp
enum class ImlRenderingMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Fallback | 0 | Если для объекта чернил (InkML) доступна резервная форма, Aspose.Words отображает резервную форму вместо InkML. |
| InkML | 1 | Aspose.Words игнорирует резервную форму объекта чернил (InkML) и рендерит сам InkML. Это режим по умолчанию. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
