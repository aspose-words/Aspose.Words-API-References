---
title: "Aspose::Words::Font::get_LineSpacing yöntemi"
linktitle: "get_LineSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_LineSpacing yöntemi. Bu yazı tipinin satır aralığını (nokta cinsinden) C++'de döndürür."
type: docs
weight: 21000
url: /tr/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Bu yazı tipinin satır aralığını (puan cinsinden) döndürür.

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Örnekler



Yazı tipinin satır aralığını nokta cinsinden nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// DocumentBuilder için farklı yazı tipleri ayarlayın ve satır aralıklarını doğrulayın.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
