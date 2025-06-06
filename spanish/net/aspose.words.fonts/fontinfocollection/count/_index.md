---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontInfoCollection Count, recupere sin esfuerzo el número total de elementos en su colección para una gestión de datos perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Obtiene el número de elementos contenidos en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra información sobre las fuentes que están presentes en el documento en blanco.

```csharp
Document doc = new Document();

// Un documento en blanco contiene 3 fuentes predeterminadas. Cada fuente del documento
// tendrá un objeto FontInfo correspondiente que contiene detalles sobre esa fuente.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Ver también

* class [FontInfoCollection](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
