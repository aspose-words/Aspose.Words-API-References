---
title: "Aspose::Words::CleanupOptions::get_DuplicateStyle‑metod"
linktitle: "get_DuplicateStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CleanupOptions::get_DuplicateStyle metod. Hämtar/sätter en flagga som indikerar om duplicerade stilar ska tas bort från dokumentet. Standardvärdet är falskt i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Hämtar/sätter en flagga som indikerar om dubblettstilar ska tas bort från dokumentet. Standardvärdet är **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Exempel



Visar hur man tar bort duplicerade stilar från dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Lägg till två stilar i dokumentet med identiska egenskaper,
// men olika namn. Den andra stilen anses vara en duplikat av den första.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Applicera båda stilarna på olika stycken i dokumentet.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Konfigurera ett CleanOptions‑objekt och anropa sedan Cleanup‑metoden för att ersätta alla duplicerade stilar
// med originalet och ta bort duplikaten från dokumentet.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Se även

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
