---
title: "Aspose::Words::Font::get_LineSpacing Methode"
linktitle: "get_LineSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_LineSpacing Methode. Gibt den Zeilenabstand dieser Schriftart (in Punkten) in C++ zurück."
type: docs
weight: 21000
url: /de/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Gibt den Zeilenabstand dieser Schrift zurück (in Punkten).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Beispiele



Zeigt, wie man den Zeilenabstand einer Schriftart in Punkten ermittelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzt verschiedene Schriftarten für den DocumentBuilder und überprüft deren Zeilenabstand.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
