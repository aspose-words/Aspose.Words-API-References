---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat метод"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat метод. Получает или задает значение, указывающее, используется ли при разборе числового формата инвариантная культура, в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Получает или задает значение, указывающее, разбирается ли числовой формат с использованием инвариантной культуры.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Примечания


Когда это свойство установлено в **true**, числовой формат берётся из инвариантной культуры.

Когда это свойство установлено в **false**, числовой формат берётся из культуры текущего потока.

Значение по умолчанию — **false**.

## Примеры



Показывает, как форматировать числа в соответствии с инвариантной культурой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Иногда поля могут некорректно форматировать свои числа при определённых культурах.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Чтобы исправить это, мы можем изменить культуру для всего потока.
// Другой способ исправить это — установить этот флаг,
// что заставит все поля использовать инвариантную культуру при форматировании чисел.
// Таким образом мы избегаем изменения культуры для всего потока.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
