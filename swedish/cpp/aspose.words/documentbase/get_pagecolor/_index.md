---
title: "Aspose::Words::DocumentBase::get_PageColor metod"
linktitle: "get_PageColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::get_PageColor metod. Hämtar eller anger sidans färg i dokumentet. Denna egenskap är en enklare version av BackgroundShape i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Hämtar eller anger sidans färg i dokumentet. Denna egenskap är en enklare version av [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Anmärkningar


Denna egenskap ger ett enkelt sätt att ange en solid sidfärg för dokumentet. När egenskapen sätts skapas och tilldelas en lämplig [BackgroundShape](../get_backgroundshape/).

Om sidfärgen inte är angiven (t.ex. finns ingen bakgrundsform i dokumentet) returneras **Empty**.

## Exempel



Visar hur man ställer in bakgrundsfärgen för alla sidor i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Se även

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
