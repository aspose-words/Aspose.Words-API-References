---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words para .NET
description: Descubra la propiedad de granularidad de CompareOptions y controle los cambios por carácter o palabra para una edición de texto precisa. ¡Mejore el control de sus documentos hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Especifica si los cambios se rastrean por carácter o por palabra.

```csharp
public Granularity Granularity { get; set; }
```

## Observaciones

El valor predeterminado esWordLevel .

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../../)
