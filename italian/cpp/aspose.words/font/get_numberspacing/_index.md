---
title: "Aspose::Words::Font::get_NumberSpacing metodo"
linktitle: "get_NumberSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_NumberSpacing metodo. Ottiene o imposta il tipo di spaziatura del numero visualizzato in C++."
type: docs
weight: 30500
url: /it/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Ottiene o imposta il tipo di spaziatura del numero visualizzato.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Esempi



Mostra come impostare il tipo di spaziatura del numero.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Questo effetto è supportato solo nelle versioni più recenti di MS Word.
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

## Vedi anche

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
