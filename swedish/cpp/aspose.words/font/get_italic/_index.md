---
title: "Aspose::Words::Font::get_Italic metod"
linktitle: "get_Italic"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Italic metod. Sant om teckensnittet är formaterat som kursiv i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


Sant om teckensnittet är formaterat som kursiv.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Exempel



Visar hur man skriver kursiverad text med en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
