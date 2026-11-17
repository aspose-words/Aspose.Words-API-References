---
title: Aspose::Words::Font::get_LineSpacing method
linktitle: get_LineSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_LineSpacing method. Returns line spacing of this font (in points) in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Returns line spacing of this font (in points).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Examples



Shows how to get a font's line spacing, in points. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set different fonts for the DocumentBuilder and verify their line spacing.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
