---
title: "Метод Aspose::Words::Font::get_AutoColor"
linktitle: "get_AutoColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_AutoColor. Возвращает текущий вычисленный цвет текста (чёрный или белый), используемый для ''auto color''. Если цвет не ''auto'', то возвращает Color в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Возвращает текущий вычисленный цвет текста (чёрный или белый), используемый для 'auto color'. Если цвет не 'auto', то возвращает [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Примечания


Когда у текста установлен 'автоматический цвет', фактический цвет текста вычисляется автоматически, чтобы быть читаемым на фоне цвета фона. При изменении цвета фона цвет текста автоматически переключается на чёрный или белый в MS Word для максимальной разборчивости.

## Примеры



Показывает, как улучшить читаемость, автоматически выбирая цвет текста в зависимости от яркости его фона.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если объект Font в пробеге не указывает цвет текста, он будет автоматически
// выбирать либо чёрный, либо белый в зависимости от цвета фона.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// Цвет текста по умолчанию — чёрный. Если цвет фона тёмный, чёрный текст будет трудно увидеть.
// Чтобы решить эту проблему, свойство AutoColor отобразит этот текст белым.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Если мы изменим фон на светлый цвет, чёрный будет более
// подходящим цветом текста, чем белый, поэтому автоматический цвет отобразит его чёрным.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
