---
title: "Aspose::Words::Font::get_NumberSpacing metod"
linktitle: "get_NumberSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_NumberSpacing metod. Hämtar eller anger typ av avstånd för siffran som visas i C++."
type: docs
weight: 30500
url: /sv/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Hämtar eller anger avståndstypen för det tal som visas.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Exempel



Visar hur man ställer in avståndstypen för siffran.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Denna effekt stöds endast i nyare versioner av MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Se även

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
