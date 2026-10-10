---
title: "Aspose::Words::Style::get_BuiltIn metod"
linktitle: "get_BuiltIn"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_BuiltIn metod. Sant om den här stilen är en av de inbyggda stilarna i MS Word i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Sant om denna stil är en av de inbyggda stilarna i MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Exempel



Visar hur man skiljer anpassade stilar från inbyggda stilar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// När vi skapar ett dokument med Microsoft Word, eller programatiskt med Aspose.Words,
// kommer dokumentet med en samling stilar som kan tillämpas på dess text för att ändra dess utseende.
// Vi kan komma åt dessa inbyggda stilar via dokumentets "Styles"‑samling.
// Dessa stilar kommer alla att ha flaggan "BuiltIn" satt till "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Skapa en anpassad stil och lägg till den i samlingen.
// Anpassade stilar som denna kommer att ha flaggan "BuiltIn" satt till "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
