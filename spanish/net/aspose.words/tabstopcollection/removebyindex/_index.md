---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words para .NET
description: TabStopCollection RemoveByIndex método. Elimina una tabulación en el índice especificado de la colección en C#.
type: docs
weight: 110
url: /es/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Elimina una tabulación en el índice especificado de la colección.

```csharp
public void RemoveByIndex(int index)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | Un índice de la colección de tabulaciones. |

## Ejemplos

Muestra cómo seleccionar una tabulación en un documento por su índice y eliminarla.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Elimina la primera tabulación.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Ver también

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
