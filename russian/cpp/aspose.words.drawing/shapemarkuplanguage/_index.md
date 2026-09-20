---
title: "Перечисление Aspose::Words::Drawing::ShapeMarkupLanguage"
linktitle: "ShapeMarkupLanguage"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::ShapeMarkupLanguage. Указывает язык разметки, используемый для фигуры в C++."
type: docs
weight: 37000
url: /ru/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


Указывает язык [Разметка](../../aspose.words.markup/), используемый для фигуры.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Разметка](../../aspose.words.markup/) язык используется для определения фигуры. |
| Vml | 1 | Векторный [Разметка](../../aspose.words.markup/) язык используется для определения фигуры. |


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

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
