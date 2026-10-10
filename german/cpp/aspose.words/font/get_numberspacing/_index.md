---
title: "Aspose::Words::Font::get_NumberSpacing Methode"
linktitle: "get_NumberSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_NumberSpacing Methode. Ruft den Abstandstyp der angezeigten Ziffer ab oder legt ihn fest in C++."
type: docs
weight: 30500
url: /de/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Liest oder legt den Abstandstyp der angezeigten Ziffer fest.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Beispiele



Zeigt, wie der Abstandstyp der Ziffer festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dieser Effekt wird nur in neueren Versionen von MS Word unterstützt.
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

## Siehe auch

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
