---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words para .NET
description: BuiltInDocumentProperties TitlesOfParts propiedad. Cada cadena de la matriz especifica el nombre de una parte del documento en C#.
type: docs
weight: 300
url: /es/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Cada cadena de la matriz especifica el nombre de una parte del documento.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Observaciones

Aspose.Words no actualiza esta propiedad.

## Ejemplos

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
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
