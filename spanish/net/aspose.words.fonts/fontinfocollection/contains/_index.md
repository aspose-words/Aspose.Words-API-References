---
title: FontInfoCollection.Contains
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfoCollection método. Determina si la colección contiene una fuente con el nombre dado.
type: docs
weight: 60
url: /es/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Determina si la colección contiene una fuente con el nombre dado.

```csharp
public bool Contains(string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | Nombre que no distingue entre mayúsculas y minúsculas de la fuente a localizar. |

### Valor_devuelto

True si el elemento se encuentra en la colección; en caso contrario, falso.

### Ejemplos

Muestra información sobre las fuentes que están presentes en el documento en blanco.

```csharp
Document doc = new Document();

// Un documento en blanco contiene 3 fuentes predeterminadas. Cada fuente en el documento
// tendrá un objeto FontInfo correspondiente que contiene detalles sobre esa fuente.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Ver también

* class [FontInfoCollection](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontinfocollection/)
* asamblea [Aspose.Words](../../../)


