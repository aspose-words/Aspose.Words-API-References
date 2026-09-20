---
title: "Enumeración Aspose::Words::Settings::MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Settings::MultiplePagesType. Especifica cómo se imprime el documento en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Especifica cómo se imprime el documento.

```cpp
enum class MultiplePagesType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | 0 | Impresión normal, sin páginas múltiples especificadas. |
| MirrorMargins | 1 | Intercambia los márgenes izquierdo y derecho en páginas opuestas. |
| TwoPagesPerSheet | 2 | Imprime dos páginas por hoja. |
| BookFoldPrinting | 3 | Especifica si se debe imprimir el documento como un pliegue de libro. |
| BookFoldPrintingReverse | 4 | Especifica si se debe imprimir el documento como un pliegue de libro inverso. |
| Default | n/a | El valor predeterminado es [Normal](./) |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
