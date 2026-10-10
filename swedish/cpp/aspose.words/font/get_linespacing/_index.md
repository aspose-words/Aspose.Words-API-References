---
title: "Aspose::Words::Font::get_LineSpacing metod"
linktitle: "get_LineSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_LineSpacing metod. Returnerar radavståndet för detta teckensnitt (i punkter) i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Returnerar radavståndet för detta teckensnitt (i punkter).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Exempel



Visar hur man får ett teckensnitts radavstånd, i punkter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in olika teckensnitt för DocumentBuilder och verifiera deras radavstånd.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
