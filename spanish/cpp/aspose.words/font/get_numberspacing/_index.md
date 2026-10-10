---
title: "Método Aspose::Words::Font::get_NumberSpacing"
linktitle: "get_NumberSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_NumberSpacing. Obtiene o establece el tipo de espaciado del número que se muestra en C++."
type: docs
weight: 30500
url: /es/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Obtiene o establece el tipo de espaciado del número que se muestra.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Ejemplos



Muestra cómo establecer el tipo de espaciado del numeral.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Este efecto solo es compatible con versiones más recientes de MS Word.
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

## Ver también

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
