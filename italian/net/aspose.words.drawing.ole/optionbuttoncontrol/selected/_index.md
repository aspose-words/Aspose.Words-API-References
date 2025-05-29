---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words per .NET
description: Gestisci il tuo OptionButtonControl con facilità! Imposta o ottieni il suo stato selezionato con un semplice valore booleano per un'interazione utente fluida.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Ottiene o imposta un valore booleano che indica questo[`OptionButtonControl`](../) è selezionato o meno.

```csharp
public bool Selected { get; set; }
```

## Osservazioni

Nota, questa proprietà consente di selezionare più elementi in un gruppo di[`OptionButtonControl`](../) con lo stesso[`GroupName`](../../forms2olecontrol/groupname/) Sta a te occuparti di deselezionare un elemento precedentemente selezionato quando esegui questa operazione[`OptionButtonControl`](../) selezionato.

## Esempi

Mostra come selezionare il pulsante di scelta.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Deseleziona il primo elemento selezionato.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Seleziona il secondo pulsante di opzione.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Guarda anche

* class [OptionButtonControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
