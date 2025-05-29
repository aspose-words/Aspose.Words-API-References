---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Comparing.Granularity para rastrear fácilmente los cambios en los documentos con precisión. ¡Mejore su comparación de documentos hoy mismo!
type: docs
weight: 490
url: /es/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Especifica la granularidad de los cambios a seguir al comparar dos documentos.

```csharp
public enum Granularity
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| CharLevel | `0` | Especifica cambios a nivel de personaje. |
| WordLevel | `1` | Especifica cambios a nivel de palabra. |

## Ejemplos

Muestra cómo especificar una granularidad al comparar documentos.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Especifique si se están realizando seguimientos de los cambios
// por carácter ('Granularity.CharLevel'), o por palabra ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La colección de grupos de revisión del primer documento contiene todas las diferencias entre los documentos.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../)
