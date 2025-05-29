---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words para .NET
description: Descubre el método GetPositionByIndex de TabStopCollection para encontrar fácilmente las posiciones de tabulación en puntos por índice. ¡Optimiza tu diseño sin esfuerzo!
type: docs
weight: 100
url: /es/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Obtiene la posición (en puntos) de la tabulación en el índice especificado.

```csharp
public double GetPositionByIndex(int index)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | Un índice de la colección de tabulaciones. |

### Valor_devuelto

La posición de la tabulación.

## Ejemplos

Muestra cómo encontrar una pestaña, pasar por su índice y verificar su posición.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Verificar la posición de la segunda tabulación en la colección.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Ver también

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
