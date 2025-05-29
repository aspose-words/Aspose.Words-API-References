---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.TextBoxControl per visualizzare facilmente testo organizzato a partire da dati o input utente. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 1520
url: /it/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

Il controllo TextBox visualizza il testo da un set organizzato di dati o input utente.

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Ottiene o imposta un testo del controllo. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Ottiene il tipo di controllo Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ottiene la proprietà Value sottostante che spesso rappresenta lo stato di controllo. Ad esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ottiene o imposta la larghezza del controllo in punti. |

## Esempi

Mostra come modificare il testo del controllo OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Guarda anche

* class [MorphDataControl](../morphdatacontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
