---
title: "Aspose::Words::ControlChar::Cr método"
linktitle: "Cr"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ControlChar::Cr método. Carácter de retorno de carro: \"\\x000d\" o \"\\r\". Igual que ParagraphBreak en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Carácter de retorno de carro: "\x000d" o "\r". Igual que [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Ejemplos



Muestra cómo usar caracteres de control.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta párrafos con texto usando DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Convertir el documento a formato de texto revela que los caracteres de control
// representan algunos de los elementos estructurales del documento, como saltos de página.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Al convertir un documento a forma de cadena,
// podemos omitir algunos de los caracteres de control con el método Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Ver también

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
