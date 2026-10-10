---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage método"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage método. Obtiene o establece un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a NewPage de forma forzada al llamar a AppendDocument(). El valor predeterminado es true en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Obtiene o establece un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [NewPage](../../sectionstart/) de forma forzada al llamar a [AppendDocument()](../). El valor predeterminado es **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Ejemplos



Muestra cómo preservar el tipo de sección original.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
