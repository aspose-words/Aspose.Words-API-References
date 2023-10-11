---
title: BuiltInDocumentProperties.HeadingPairs
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Especifica los títulos de los documentos y sus nombres.
type: docs
weight: 110
url: /es/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Especifica los títulos de los documentos y sus nombres.

```csharp
public object[] HeadingPairs { get; set; }
```

### Observaciones

Cada par de encabezados ocupa dos elementos en esta matriz.

El primer elemento del par es unString y especifica el nombre del encabezado. El segundo elemento del par es unInt32 y especifica el recuento de document partes para este encabezado en el[`TitlesOfParts`](../titlesofparts/) propiedad.

La suma total de recuentos de todos los pares de encabezados en esta propiedad debe ser igual al número de elementos en el[`TitlesOfParts`](../titlesofparts/) propiedad.

Aspose.Words no actualiza esta propiedad.

### Ejemplos

Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Podemos encontrar los valores combinados de estas colecciones vía
// "Archivo" -> "Propiedades" -> "Propiedades avanzadas" -> Pestaña "Contenidos".
// La propiedad HeadingPairs es una colección de <string, int> pares que
// determina cuántas partes del documento abarca un encabezado.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// La propiedad TitlesOfParts contiene los nombres de las partes que pertenecen a los encabezados anteriores.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../builtindocumentproperties/)
* asamblea [Aspose.Words](../../../)


