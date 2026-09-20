---
title: "Конструктор Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions"
linktitle: "OoxmlSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions конструктор. Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате Docx в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Docx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
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

## См. также

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) или [FlatOpc](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Может быть [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) или [FlatOpc](../../../aspose.words/saveformat/). |

## Примеры



Показывает, как поддерживать устаревшие управляющие символы при конвертации в .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Когда мы сохраняем документ в формат OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передать его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство \"KeepLegacyControlChars\" в \"true\", чтобы сохранить
// устаревший символ \"ShortDateTime\" при сохранении.
// Установите свойство \"KeepLegacyControlChars\" в \"false\", чтобы удалить
// устаревший символ \"ShortDateTime\" из выходного документа.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
