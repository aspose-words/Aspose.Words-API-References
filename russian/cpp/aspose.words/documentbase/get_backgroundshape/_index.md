---
title: "Метод Aspose::Words::DocumentBase::get_BackgroundShape"
linktitle: "get_BackgroundShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBase::get_BackgroundShape. Получает или задает форму фона документа. Может быть null в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Получает или задает форму фона документа. Может быть **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Примечания


Microsoft Word допускает только форму, у которой свойство [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) равно [Rectangle](../../../aspose.words.drawing/shapetype/), для использования в качестве формы фона документа.

Microsoft Word поддерживает только свойства заливки формы фона. Все остальные свойства игнорируются.

Установка этого свойства в ненулевое значение также установит [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) в **true**.

## Примеры



Показывает, как задать форму фона для каждой страницы документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// Единственный тип формы, который мы можем использовать в качестве фона, — прямоугольник.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Существует два способа использования этой формы в качестве фона страницы.
// 1 -  Плоский цвет:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Изображение:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Отрегулируйте внешний вид изображения, чтобы сделать его более подходящим в качестве водяного знака.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word не поддерживает формы с изображениями в качестве фона,
// но мы всё равно можем видеть эти фоны в других форматах сохранения, таких как .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
