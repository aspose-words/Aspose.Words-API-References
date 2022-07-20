---
title: Granularity
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel .
type: docs
weight: 20
url: /es/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

### Ejemplos

Muestra para especificar una granularidad al comparar documentos.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Especificar si los cambios son de seguimiento
// por carácter ('Granularity.CharLevel'), o por palabra ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La colección de grupos de revisión del primer documento contiene todas las diferencias entre documentos.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Ver también

* enum [Granularity](../../granularity)
* class [CompareOptions](../../compareoptions)
* espacio de nombres [Aspose.Words.Comparing](../../compareoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->