---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture метод"
linktitle: "get_PreProcessCulture"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture метод. Получает или задает культуру для предварительной обработки значений полей в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Получает или задает культуру для предварительной обработки значений полей.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Примечания


В настоящее время это свойство влияет только на значение поля [FieldDocProperty](../../fielddocproperty/).

Значение по умолчанию — **null**. Когда это свойство установлено в **null**, значение поля [FieldDocProperty](../../fielddocproperty/) предварительно обрабатывается культурой, управляемой свойством [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## Примеры



Показывает, как установить культуру предварительной обработки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите культуру, в соответствии с которой некоторые поля будут форматировать отображаемые значения.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// Поле DOCPROPERTY будет отображать свой результат, отформатированный в соответствии с культурой предварительной обработки
// мы установили её на немецкую. Поле будет отображать дату/время в формате "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// После переключения на инвариантную культуру поле DOCPROPERTY будет использовать формат "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
