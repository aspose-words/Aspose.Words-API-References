---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Ole.Forms2OleControl, la soluzione per integrare perfettamente i controlli OLE di Microsoft Forms 2.0 nelle tue applicazioni.
type: docs
weight: 1460
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Rappresenta il controllo OLE di Microsoft Forms 2.0.

Per saperne di più, visita il[Lavorare con oggetti Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) articolo di documentazione.

```csharp
public abstract class Forms2OleControl : OleControl
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
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Restituisce`VERO` se il controllo è un`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ottiene o imposta il nome del controllo ActiveX. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Ottiene il tipo di controllo Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ottiene la proprietà Value sottostante che spesso rappresenta lo stato di controllo. Ad esempio, il pulsante di opzione selezionato ha valore '1' mentre quello non selezionato ha valore '0'. Il valore predefinito è una stringa vuota. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ottiene o imposta la larghezza del controllo in punti. |

## Esempi

Mostra come verificare le proprietà di un controllo ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Nota che non puoi impostare GroupName per un Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### Guarda anche

* class [OleControl](../olecontrol/)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../)
