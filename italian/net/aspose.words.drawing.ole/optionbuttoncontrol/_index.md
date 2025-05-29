---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.OptionButtonControl, perfetta per creare opzioni di scelta esclusive nelle tue applicazioni. Migliora l'esperienza utente oggi stesso!
type: docs
weight: 1510
url: /it/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

Il controllo OptionButton consente una singola scelta in un set limitato di scelte reciprocamente esclusive.

```csharp
public class OptionButtonControl : MorphDataControl
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Ottiene o imposta un colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Ottiene o imposta una proprietà Caption del controllo. Il valore predefinito è una stringa vuota. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Ottiene la raccolta di controlli figlio immediati. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Restituisce`VERO` se il controllo è nello stato abilitato. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Ottiene o imposta un colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Ottiene o imposta una stringa che specifica un gruppo di controlli reciprocamente esclusivi. Il valore predefinito è una stringa vuota. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Ottiene o imposta l'altezza del controllo in punti. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Restituisce`VERO` se il controllo è un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ottiene o imposta il nome del controllo ActiveX. |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Ottiene o imposta un valore booleano che indica questo`OptionButtonControl` è selezionato o meno. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Ottiene il tipo di controllo Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ottiene la proprietà Value sottostante che spesso rappresenta lo stato di controllo. Ad esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ottiene o imposta la larghezza del controllo in punti. |

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

* class [MorphDataControl](../morphdatacontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
