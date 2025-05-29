---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words para .NET
description: Descubra el método HasSameTemplate, verifique fácilmente si dos listas comparten la misma plantilla, asegurando consistencia y eficiencia en la gestión de sus datos.
type: docs
weight: 120
url: /es/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Devuelve verdadero si la lista actual y la lista dada se crean a partir de la misma plantilla.

```csharp
public bool HasSameTemplate(List other)
```

## Ejemplos

Muestra cómo definir listas con el mismo ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Ver también

* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
