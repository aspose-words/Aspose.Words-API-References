---
title: "Aspose::Words::Section::ClearContent method"
linktitle: "ClearContent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::ClearContent method. Rensar avsnittet i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Rensar avsnittet.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Anmärkningar


Texten i [Body](../get_body/) rensas, endast ett tomt stycke återstår som representerar avsnittsbrytningen.

Texten i alla sidhuvuden och sidfötter rensas, men [HeaderFooter](../../headerfooter/)-objekten själva tas inte bort.

## Exempel



Visar hur man rensar innehållet i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Att köra metoden \"ClearContent\" kommer att ta bort allt avsnittsinnehåll
// men lämna ett tomt stycke för att kunna lägga till innehåll igen.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Se även

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
