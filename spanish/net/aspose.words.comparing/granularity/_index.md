---
title: Enum Granularity
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Comparing.Granularity enumeración. Especifica la granularidad de los cambios que se deben rastrear al comparar dos documentos.
type: docs
weight: 290
url: /es/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Especifica la granularidad de los cambios que se deben rastrear al comparar dos documentos.

```csharp
public enum Granularity
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

### Ejemplos

Muestra para especificar una granularidad al comparar documentos.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Especifica si los cambios son de seguimiento
// por carácter ('Granularity.CharLevel') o por palabra ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La colección de grupos de revisión del primer documento contiene todas las diferencias entre documentos.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../)


