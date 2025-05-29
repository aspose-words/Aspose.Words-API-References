---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words para .NET
description: Descubre si FontInfoCollection incluye una fuente específica por nombre. Gestiona y accede fácilmente a tu colección de fuentes con este método esencial.
type: docs
weight: 60
url: /es/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Determina si la colección contiene una fuente con el nombre especificado.

```csharp
public bool Contains(string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | Nombre de la fuente a localizar que no distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

`verdadero`si el artículo se encuentra en la colección; de lo contrario,`FALSO`.

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
