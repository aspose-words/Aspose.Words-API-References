---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer метод"
linktitle: "GetMathRenderer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer метод. Создаёт и возвращает объект, который можно использовать для рендеринга этого уравнения в изображение в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Создаёт и возвращает объект, который можно использовать для рендеринга этого уравнения в изображение.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

Объект рендерера для этого уравнения.
## Примечания


Этот метод просто вызывает конструктор [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) и передаёт этот объект в качестве параметра.

## Примеры



Показывает, как отрендерить объект Office [Math](../../) в файл изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Создайте объект "ImageSaveOptions", чтобы передать его методу "Save" рендерера узла для изменения
// как он рендерит узел OfficeMath в изображение.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Установите свойство "Scale" в 5, чтобы отрендерить объект в пять раз больше его исходного размера.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## См. также

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
