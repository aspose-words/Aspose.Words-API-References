---
title: "Aspose::Words::CleanupOptions::get_DuplicateStyle метод"
linktitle: "get_DuplicateStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::CleanupOptions::get_DuplicateStyle метод. Получает/устанавливает флаг, указывающий, следует ли удалять дублирующие стили из документа. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Получает/устанавливает флаг, указывающий, следует ли удалять дублирующие стили из документа. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Примеры



Показывает, как удалить дублирующие стили из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Добавьте два стиля в документ с идентичными свойствами,
// но разными именами. Второй стиль считается дубликатом первого.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Примените оба стиля к разным абзацам в документе.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Настройте объект CleanOptions, затем вызовите метод Cleanup, чтобы заменить все дублирующие стили
// на оригинальные и удалить дубликаты из документа.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## См. также

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
