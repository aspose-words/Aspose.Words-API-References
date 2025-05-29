---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.CheckBoxControl per alternare facilmente i valori delle caselle di controllo e migliorare l'automazione dei tuoi documenti con un'integrazione perfetta.
type: docs
weight: 1440
url: /it/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

Il controllo CheckBox commuta un valore.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Ottiene o imposta un colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Ottiene o imposta una proprietà Caption del controllo. Il valore predefinito è una stringa vuota. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Ottiene o imposta un valore booleano che indica questo`CheckBoxControl` è selezionato o meno. Il valore predefinito è`falso` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Ottiene la raccolta di controlli figlio immediati. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Restituisce`VERO` se il controllo è nello stato abilitato. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Ottiene o imposta un colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Ottiene o imposta una stringa che specifica un gruppo di controlli reciprocamente esclusivi. Il valore predefinito è una stringa vuota. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Ottiene o imposta l'altezza del controllo in punti. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Restituisce`VERO` se il controllo è un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ottiene o imposta il nome del controllo ActiveX. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Ottiene il tipo di controllo Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ottiene la proprietà Value sottostante che spesso rappresenta lo stato di controllo. Ad esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ottiene o imposta la larghezza del controllo in punti. |

## Osservazioni

Ha tre possibili stati: selezionato, deselezionato e né selezionato né deselezionato, ovvero una combinazione di stati acceso e spento.

## Esempi

Mostra come modificare lo stato del controllo CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Guarda anche

* class [MorphDataControl](../morphdatacontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
