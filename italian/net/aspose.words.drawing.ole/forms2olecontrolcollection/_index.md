---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.Forms2OleControlCollection, la soluzione per gestire in modo efficiente gli oggetti Forms2OleControl nell'elaborazione dei documenti.
type: docs
weight: 1470
url: /it/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Rappresenta la raccolta di[`Forms2OleControl`](../forms2olecontrol/) oggetti.

Per saperne di più, visita il[Lavorare con oggetti Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) articolo di documentazione.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Ottiene il conteggio degli oggetti nella raccolta. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Ottiene[`Forms2OleControl`](../forms2olecontrol/) oggetto a un indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Ottiene l'enumeratore. |

## Esempi

Mostra come accedere a un controllo OLE incorporato in un documento e ai suoi controlli figlio.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Le forme memorizzano e visualizzano gli oggetti OLE nel corpo del documento.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Alcuni controlli OLE possono contenere controlli figlio, come quello in questo documento con tre pulsanti di opzione.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Guarda anche

* class [Forms2OleControl](../forms2olecontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
