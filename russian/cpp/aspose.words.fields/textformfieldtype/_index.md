---
title: "Aspose::Words::Fields::TextFormFieldType перечисление"
linktitle: "TextFormFieldType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::TextFormFieldType перечисление. Указывает тип текстового поля формы в C++."
type: docs
weight: 134000
url: /ru/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Указывает тип текстового поля формы.

```cpp
enum class TextFormFieldType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Regular | 0 | Текстовое поле формы может содержать любой текст. |
| Number | 1 | Текстовое поле формы может содержать только числа. |
| Дата | 2 | Текстовое поле формы может содержать только корректное значение даты. |
| CurrentDate | 3 | Значение текстового поля формы — текущая дата при обновлении поля. |
| CurrentTime | 4 | Значение текстового поля формы — текущее время при обновлении поля. |
| Calculated | 5 | Значение текстового поля формы рассчитывается из выражения, указанного в свойстве [TextInputDefault](../formfield/get_textinputdefault/). |


## Примеры



Показывает, как создавать поля формы.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Поля формы — это объекты в документе, с которыми пользователь может взаимодействовать, получая запрос на ввод значений.
// Мы можем создавать их с помощью построителя документов, а ниже представлены два способа сделать это.
// 1 -  Базовый ввод текста:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Выпадающий список с подсказкой и диапазоном возможных значений:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
