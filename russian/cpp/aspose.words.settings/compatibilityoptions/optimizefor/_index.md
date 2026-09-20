---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor метод"
linktitle: "OptimizeFor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor method. Позволяет оптимизировать содержимое документа, а также поведение Aspose.Words по умолчанию для определённых версий MS Word. Используйте этот метод, чтобы предотвратить отображение ленты \"Compatibility mode\" в MS Word при загрузке документа. (Обратите внимание, что также может потребоваться установить свойство Compliance в Iso29500_2008_Transitional или выше.) в C++."
type: docs
weight: 75000
url: /ru/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Позволяет оптимизировать содержимое документа, а также поведение Aspose.Words по умолчанию для определённых версий MS Word. Используйте этот метод, чтобы предотвратить отображение ленты "Compatibility mode" в MS Word при загрузке документа. (Обратите внимание, что также может потребоваться установить свойство [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) в значение [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) или выше.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
```


## Примеры



Показывает, как задать спецификацию соответствия OOXML для сохраняемого документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если мы настроим параметры совместимости для соответствия Microsoft Word 2003,
// вставка изображения определит его форму с использованием VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Стандарт OOXML "ISO/IEC 29500:2008" не поддерживает формы VML.
// Если мы установим свойство "Compliance" объекта SaveOptions в значение "OoxmlCompliance.Iso29500_2008_Strict",
// любой документ, сохраняемый с этим объектом, должен будет соответствовать этому стандарту.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Наш сохраняемый документ определяет форму с использованием DML, чтобы соответствовать стандарту OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Показывает, как вертикально выровнять текстовое содержимое текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Top", чтобы
// выравнять текст в этом текстовом поле по верхней стороне фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Middle", чтобы
// выравнять текст в этом текстовом поле по центру фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Bottom", чтобы
// выравнять текст в этом текстовом поле по нижней части фигуры.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно, начиная с Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## См. также

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
