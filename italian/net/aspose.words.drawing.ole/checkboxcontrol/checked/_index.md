---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words per .NET
description: Scopri la proprietà CheckBoxControl Checked, gestisci facilmente gli stati delle caselle di controllo con un semplice valore booleano. Il valore predefinito è "false" per un controllo ottimale.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Ottiene o imposta un valore booleano che indica questo[`CheckBoxControl`](../) è selezionato o meno. Il valore predefinito è`falso` .

```csharp
public bool Checked { get; set; }
```

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

* class [CheckBoxControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
