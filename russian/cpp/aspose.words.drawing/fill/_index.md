---
title: "Класс Aspose::Words::Drawing::Fill"
linktitle: "Fill"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::Fill. Представляет форматирование заливки для объекта. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.drawing/fill/
---
## Fill class


Представляет форматирование заливки для объекта. Чтобы узнать больше, посетите статью документации [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Получает или задает объект Color, который представляет цвет фона заливки. |
| [get_BackThemeColor](./get_backthemecolor/)() | Получает или задает объект ThemeColor, который представляет цвет фона заливки. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Получает или задает значение типа double, которое осветляет или затемняет цвет фона. |
| [get_BaseForeColor](./get_baseforecolor/)() | Получает объект Color, который представляет базовый цвет переднего плана заливки без каких-либо модификаторов. |
| [get_Color](./get_color/)() | Получает или задает объект Color, который представляет цвет переднего плана заливки. |
| [get_FillType](./get_filltype/)() | Получает тип заливки. |
| [get_ForeColor](./get_forecolor/)() | Получает объект Color, который представляет цвет переднего плана заливки. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Получает или задает объект ThemeColor, который представляет цвет переднего плана заливки. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана. |
| [get_GradientAngle](./get_gradientangle/)() | Получает или задает угол градиентной заливки. |
| [get_GradientStops](./get_gradientstops/)() | Получает коллекцию объектов [GradientStop](../gradientstop/) для заливки. |
| [get_GradientStyle](./get_gradientstyle/)() | Получает стиль градиента [GradientStyle](../gradientstyle/) для заливки. |
| [get_GradientVariant](./get_gradientvariant/)() | Получает вариант градиента [GradientVariant](../gradientvariant/) для заливки. |
| [get_ImageBytes](./get_imagebytes/)() | Получает необработанные байты текстуры или узора заливки. |
| [get_Opacity](./get_opacity/)() | Получает или задает степень непрозрачности указанной заливки как значение от 0.0 (прозрачная) до 1.0 (непрозрачная). |
| [get_Pattern](./get_pattern/)() | Получает [PatternType](../patterntype/) для заливки. |
| [get_PresetTexture](./get_presettexture/)() | Получает [PresetTexture](../presettexture/) для заливки. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Получает, вращается ли заливка вместе с указанным объектом. |
| [get_TextureAlignment](./get_texturealignment/)() | Получает или задает выравнивание для плиточной текстурной заливки. |
| [get_Transparency](./get_transparency/)() | Получает или задает степень прозрачности указанной заливки как значение от 0.0 (непрозрачная) до 1.0 (прозрачная). |
| [get_Visible](./get_visible/)() | Получает значение, которое **true**, если примененное к этому экземпляру форматирование видно. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Устанавливает указанную заливку в одноцветный градиент. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Устанавливает указанную заливку в одноцветный градиент, используя указанный цвет. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Устанавливает указанную заливку в узор. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Устанавливает указанную заливку в узор. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Устанавливает заливку в предустановленную текстуру. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Сеттер для [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Устанавливает объект Color, представляющий цвет переднего плана для заливки. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Сеттер для [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Сеттер для [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Сеттер для [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Сеттер для [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Устанавливает, будет ли заливка вращаться вместе с указанным объектом. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Сеттер для [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Сеттер для [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Устанавливает значение, которое **true**, если форматирование, применённое к этому экземпляру, видно. |
| [SetImage](./setimage/)(const System::String\&) | Изменяет тип заливки на одиночное изображение. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Изменяет тип заливки на одиночное изображение. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Изменяет тип заливки на одиночное изображение. |
| [Solid](./solid/)() | Устанавливает заливку в однородный цвет. |
| [Solid](./solid/)(System::Drawing::Color) | Устанавливает заливку в указанный однородный цвет. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Устанавливает указанную заливку в градиент из двух цветов. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Устанавливает указанную заливку в градиент из двух цветов. |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [Fill](../shapebase/get_fill/) или [Fill](../../aspose.words/font/get_fill/) для доступа к свойствам заливки объекта. Вы не создаёте экземпляры класса [Fill](./) напрямую.

## Примеры



Показывает, как залить форму сплошным цветом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Напишите некоторый текст, а затем накройте его плавающей формой.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Используйте свойство "StrokeColor" для установки цвета контура формы.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Используйте свойство "FillColor" для установки цвета внутренней области формы.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Свойство "Opacity" определяет, насколько прозрачным является цвет по шкале от 0 до 1,
// где 1 означает полностью непрозрачный, а 0 — невидимый.
// Заполнение фигуры по умолчанию полностью непрозрачно, поэтому мы не видим текст, который находится под этой фигурой.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Установите более низкую непрозрачность цвета заполнения фигуры, чтобы мы могли видеть текст под ней.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
