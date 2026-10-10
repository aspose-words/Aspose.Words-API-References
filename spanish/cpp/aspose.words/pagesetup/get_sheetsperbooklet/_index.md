---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet método"
linktitle: "get_SheetsPerBooklet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet método. Devuelve o establece el número de páginas que se incluirán en cada folleto en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Devuelve o establece el número de páginas que se incluirán en cada folleto.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Ejemplos



Muestra cómo configurar un documento que se puede imprimir como un pliegue de libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte texto que abarque 16 páginas.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de pliegue de libro.
// Cuando imprimimos este documento a doble cara, podemos tomar las páginas para apilarlas
// y doblarlas todas por la mitad de una vez. El contenido del documento se alineará en un pliegue de libro.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
