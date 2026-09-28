---
title: "Метод Aspose::Words::Fields::FormField::get_Result"
linktitle: "get_Result"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FormField::get_Result. Получает или задает строку, представляющую результат этого поля формы в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Получает или задает строку, представляющую результат этого поля формы.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Примечания


Для текстового поля формы результат — это текст, находящийся в поле.

Для поля формы‑чекбокса результат может быть "1" или "0", указывая на отмечено или не отмечено.

Для выпадающего списка результат — это выбранная строка.

Установка [Result](./) для текстового поля формы не применяет текстовый формат, указанный в [TextInputFormat](../get_textinputformat/). Если нужно задать значение и применить формат, используйте метод [SetTextInputValue()](../).

Для текстового поля формы значение [TextInputDefault](../get_textinputdefault/) применяется, если *value* равно **null**.

## Примеры



Показывает, как вставить комбобокс.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Вставьте комбобокс, который позволит пользователю выбрать вариант из набора строк.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Поле формы будет отображаться в виде HTML‑тега "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## См. также

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
