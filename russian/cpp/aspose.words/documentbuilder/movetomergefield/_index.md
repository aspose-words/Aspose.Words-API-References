---
title: "Метод Aspose::Words::DocumentBuilder::MoveToMergeField"
linktitle: "MoveToMergeField"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::MoveToMergeField. Перемещает курсор в позицию сразу за указанным полем слияния и удаляет поле слияния в C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Перемещает курсор в позицию сразу после указанного поля слияния и удаляет поле слияния.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | const System::String\& | Регистронезависимое имя поля слияния почты. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Примечания


Обратите внимание, что этот метод удаляет поле слияния из документа после перемещения курсора.

## Примеры



Показывает, как заполнять MERGEFIELDы данными с помощью DocumentBuilder вместо слияния почты.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте несколько MERGEFIELDов, которые принимают данные из столбцов с тем же именем в источнике данных во время слияния почты,
// а затем заполните их вручную.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Перемещает поле слияния в указанное поле слияния.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | const System::String\& | Регистронезависимое имя поля слияния почты. |
| isAfter | bool | Когда **true**, перемещает курсор после конца поля. Когда **false**, перемещает курсор перед началом поля. |
| isDeleteField | bool | Когда **true**, удаляет поле слияния. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## Примеры



Показывает, как вставлять поля и перемещать курсор построителя документа к ним.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Переместите курсор к первому MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Обратите внимание, что курсор размещён сразу после первого MERGEFIELD и перед вторым.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Если мы хотим отредактировать код поля или его содержимое с помощью построителя,
// его курсор должен находиться внутри поля.
// Чтобы разместить его внутри поля, нам нужно вызвать метод MoveTo построителя документа
// и передать в качестве аргумента начальный или разделительный узел поля.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
