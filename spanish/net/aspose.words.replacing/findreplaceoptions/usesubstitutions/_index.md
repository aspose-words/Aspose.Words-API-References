---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words para .NET
description: FindReplaceOptions UseSubstitutions propiedad. Obtiene o establece un valor booleano que indica si se reconocen y utilizan sustituciones dentro de los patrones de reemplazo. El valor predeterminado esFALSO  en C#.
type: docs
weight: 180
url: /es/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Obtiene o establece un valor booleano que indica si se reconocen y utilizan sustituciones dentro de los patrones de reemplazo. El valor predeterminado es`FALSO` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Observaciones

Para obtener detalles sobre los elementos de sustitución, consulte: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## Ejemplos

Muestra cómo reconocer y utilizar sustituciones dentro de patrones de reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// El uso del modo heredado no admite muchas funciones avanzadas, por lo que debemos configurarlo en "falso".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Muestra cómo reemplazar el texto con sustituciones.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece la propiedad "UseSubstitutions" en "true" para obtener
// la operación de buscar y reemplazar para reconocer elementos de sustitución.
// Establece la propiedad "UseSubstitutions" en "false" para ignorar los elementos de sustitución.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
