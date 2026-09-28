---
title: "Aspose::Words::Drawing::Shape::Shape constructor"
linktitle: "Shape"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::Shape constructor. Создает новый объект фигуры в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Создает новый объект формы.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
| shapeType | Aspose::Words::Drawing::ShapeType | Тип фигуры, которую нужно создать. |
## Примечания


Вам следует указать желаемые свойства формы после её создания.

## Примеры



Показывает, как вставить форму с изображением из локальной файловой системы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Публичный конструктор класса "Shape" создаст форму с типом разметки "ShapeMarkupLanguage.Vml".
// Если вам нужно создать форму нестандартного типа, например SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// пожалуйста, используйте DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Показывает, как создать и отформатировать текстовое поле.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте плавающее текстовое поле.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Установите горизонтальное и вертикальное выравнивание текста внутри фигуры.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Добавьте абзац в текстовое поле и добавьте последовательность текста, которую будет отображать текстовое поле.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## См. также

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
