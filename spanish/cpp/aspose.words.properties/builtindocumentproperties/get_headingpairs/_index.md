---
title: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs"
linktitle: "get_HeadingPairs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs. Especifica los encabezados del documento y sus nombres en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Especifica los encabezados del documento y sus nombres.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Observaciones


Cada par de encabezados ocupa dos elementos en esta matriz.

El primer elemento del par es un **String** y especifica el nombre del encabezado. El segundo elemento del par es un **Int32** y especifica el recuento de partes del documento para este encabezado en la propiedad [TitlesOfParts](../get_titlesofparts/).

La suma total de los recuentos de todos los pares de encabezados en esta propiedad debe ser igual al número de elementos en la propiedad [TitlesOfParts](../get_titlesofparts/).

Aspose.Words no actualiza esta propiedad.

## Ejemplos



Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Podemos encontrar los valores combinados de estas colecciones mediante
// "File" -> "Properties" -> "Advanced Properties" -> "Contents" pestaña.
// La propiedad HeadingPairs es una colección de pares <string, int> que
// determina cuántas partes del documento abarca un encabezado.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// La propiedad TitlesOfParts contiene los nombres de las partes que pertenecen a los encabezados anteriores.
System::ArrayPtr<System::String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int32_t headingPairsIndex = 0;
int32_t titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << System::String::Format(u"Parts for {0}:", headingPairs[headingPairsIndex++]) << std::endl;
    int32_t partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int32_t i = 0; i < partsCount; i++)
    {
        std::cout << System::String::Format(u"\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]) << std::endl;
    }
}
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
