---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words para .NET
description: CompareOptions Granularity propiedad. Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel  en C#.
type: docs
weight: 30
url: /es/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

## Ejemplos

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* espacio de nombres [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../../)
