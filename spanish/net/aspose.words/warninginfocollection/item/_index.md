---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a elementos específicos de WarningInfoCollection por índice. Optimice la gestión de sus datos con nuestra intuitiva función de propiedades.
type: docs
weight: 30
url: /es/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Obtiene un elemento en el índice especificado.

```csharp
public WarningInfo this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Índice basado en cero del artículo. |

## Ejemplos

Muestra cómo obtener advertencias sobre formatos no compatibles.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Ver también

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
