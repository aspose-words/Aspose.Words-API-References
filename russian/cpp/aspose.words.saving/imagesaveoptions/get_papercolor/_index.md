---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor метод"
linktitle: "get_PaperColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSaveOptions::get_PaperColor. Получает или задает цвет фона (бумаги) для создаваемых изображений. Значение по умолчанию — White в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Получает или задаёт цвет фона (бумаги) генерируемых изображений. Значение по умолчанию — **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Примечания


При рендеринге страниц документа, у которого указан собственный цвет фона, цвет фона документа переопределит цвет, указанный в этом свойстве.

## Примеры



Отрисовывает страницу документа Word в изображение с прозрачным или цветным фоном.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Установите свойство "PaperColor" в прозрачный цвет, чтобы применить прозрачный
// фон документа при рендеринге его в изображение.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Установите свойство "PaperColor" в непрозрачный цвет, чтобы применить этот цвет
// в качестве фона документа при его рендеринге в изображение.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## См. также

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
