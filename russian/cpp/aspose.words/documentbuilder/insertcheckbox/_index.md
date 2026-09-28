---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox method"
linktitle: "InsertCheckBox"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertCheckBox. Вставляет поле формы флажка в текущую позицию в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Вставляет поле формы с флажком в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет усечено. |
| checkedValue | bool | Отмеченное состояние поля формы флажка. |
| size | int32_t | Указывает размер флажка в пунктах. Укажите 0 для MS Word, чтобы автоматически вычислить размер флажка. |

### ReturnValue

Узел поля формы, который только что был вставлен.
## Примечания


Если указать имя для поля формы, то автоматически создаётся закладка с тем же именем.

## Примеры



Показывает, как вставить флажки в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте флажки разных размеров и с различными значениями по умолчанию.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// У полей формы ограничение длины имени в 20 символов.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щёлкнув по ним.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## См. также

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Вставляет поле формы с флажком в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | const System::String\& | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет усечено. |
| defaultValue | bool | Значение по умолчанию для поля формы‑чекбокса. |
| checkedValue | bool | Текущее состояние отметки поля формы‑чекбокса. |
| size | int32_t | Указывает размер флажка в пунктах. Укажите 0 для MS Word, чтобы автоматически вычислить размер флажка. |

### ReturnValue

Узел поля формы, который только что был вставлен.
## Примечания


Если указать имя для поля формы, то автоматически создаётся закладка с тем же именем.

## Примеры



Показывает, как вставить флажки в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте флажки разных размеров и с различными значениями по умолчанию.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// У полей формы ограничение длины имени в 20 символов.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щёлкнув по ним.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## См. также

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
