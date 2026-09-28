---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertComboBox method. Вставляет поле формы комбобокса в текущей позиции в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Вставляет поле формы с выпадающим списком в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет усечено. |
| items | const System::ArrayPtr\<System::String\>\& | Элементы ComboBox. Максимум — 25 элементов. |
| selectedIndex | int32_t | Индекс выбранного элемента в ComboBox. |

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


Показывает, как вставить поле формы комбобокса в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму, предлагающую пользователю выбрать один из пунктов меню.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## См. также

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
