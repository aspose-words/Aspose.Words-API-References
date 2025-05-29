---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words para .NET
description: Descubra el método GetIndexByPosition de TabStopCollection para encontrar fácilmente el índice de una tabulación en cualquier punto especificado. ¡Perfecto para un control preciso del diseño!
type: docs
weight: 90
url: /es/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Obtiene el índice de una tabulación con la posición especificada en puntos.

```csharp
public int GetIndexByPosition(double position)
```

## Ejemplos

Muestra cómo buscar una posición para ver si existe una tabulación allí y obtener su índice.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Agrega una tabulación en una posición de 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Un resultado de "0" devuelto por "GetIndexByPosition" confirma que hay una tabulación
// at 30mm existe en esta colección y está en el índice 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Un "-1" devuelto por "GetIndexByPosition" confirma que
// No hay tabulación en esta colección con una posición de 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Ver también

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
