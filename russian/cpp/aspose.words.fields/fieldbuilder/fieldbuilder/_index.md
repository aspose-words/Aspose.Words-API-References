---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder конструктор"
linktitle: "FieldBuilder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder конструктор. Инициализирует экземпляр класса FieldBuilder в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Инициализирует экземпляр класса [FieldBuilder](../).

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Тип поля для создания. |

## Примеры



Показывает, как создать и вставить поле с помощью построителя полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Удобный способ добавить текстовое содержимое в документ — использовать построитель документов.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// У полей есть свой построитель, который мы можем использовать для поэтапного построения кода поля.
// В этом случае мы создадим поле BARCODE, представляющее почтовый индекс США,
// а затем вставим его перед объектом Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## См. также

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
