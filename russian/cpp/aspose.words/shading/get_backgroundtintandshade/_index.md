---
title: "Aspose::Words::Shading::get_BackgroundTintAndShade метод"
linktitle: "get_BackgroundTintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Shading::get_BackgroundTintAndShade метод. Получает или задает значение типа double, которое осветляет или затемняет цвет темы фона в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


Получает или задаёт двойное значение, которое осветляет или затемняет цвет темы фона.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый темный) до 1 (самый светлый) для этого свойства.

Ноль (0) — нейтральное значение.

## Примеры



Показывает, как установить цвета переднего и заднего плана для текстуры затенения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## См. также

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
