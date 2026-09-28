---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertTextInput. Вставляет текстовое поле формы в текущую позицию в C++."
type: docs
weight: 49000
url: /ru/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Вставляет текстовое поле формы в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя текстового поля формы. Может быть пустой строкой. |
| тип | Aspose::Words::Fields::TextFormFieldType | Указывает тип текстового поля формы. |
| формат | const System::String\& | Строка формата, используемая для форматирования значения текстового поля формы. |
| fieldValue | const System::String\& | Текст, который будет отображаться в поле. |
| maxLength | int32_t | Максимальная длина, которую пользователь может ввести в текстовое поле формы. Установите 0 для неограниченной длины. |

### ReturnValue

Узел поля формы, который только что был вставлен.
## Примечания


Если указать имя для поля формы, то автоматически создаётся закладка с тем же именем.

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


Показывает, как вставить текстовое поле ввода формы в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму, которая предлагает пользователю ввести текст.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Показывает, как вставить текстовое поле ввода формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Вставьте текстовое поле ввода, которое позволит пользователю щёлкнуть по нему и ввести текст.
// Назначьте некоторый заполнитель текста, который пользователь может перезаписать и передать
// максимальная длина текста 0, чтобы не ограничивать содержимое поля формы.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Поле формы будет отображаться в виде HTML‑тега "input" с типом "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## См. также

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
