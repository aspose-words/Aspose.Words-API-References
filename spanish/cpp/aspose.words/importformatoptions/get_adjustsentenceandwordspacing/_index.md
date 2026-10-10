---
title: "método Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "método Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing. Obtiene o establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Obtiene o establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Ejemplos



Muestra cómo ajustar automáticamente el espaciado de oraciones y palabras.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
