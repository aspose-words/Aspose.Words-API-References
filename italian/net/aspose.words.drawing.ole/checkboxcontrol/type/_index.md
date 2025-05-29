---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà CheckBoxControl Type per Forms 2.0, che sblocca opzioni di controllo versatili per migliorare la funzionalità della tua applicazione.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

Ottiene il tipo di controllo Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
