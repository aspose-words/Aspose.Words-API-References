---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words per .NET
description: TabStopCollection RemoveByIndex metodo. Rimuove dalla raccolta un punto di tabulazione in corrispondenza dellindice specificato in C#.
type: docs
weight: 110
url: /it/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Rimuove dalla raccolta un punto di tabulazione in corrispondenza dell'indice specificato.

```csharp
public void RemoveByIndex(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Un indice nella raccolta di tabulazioni. |

## Esempi

Mostra come selezionare una tabulazione in un documento tramite il suo indice e rimuoverla.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Rimuove la prima tabulazione.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Guarda anche

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
