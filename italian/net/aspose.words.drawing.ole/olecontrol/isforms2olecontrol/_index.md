---
title: OleControl.IsForms2OleControl
linktitle: IsForms2OleControl
articleTitle: IsForms2OleControl
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsForms2OleControl di OleControl, che identifica se il tuo controllo è un Forms2OleControl, migliorando l'efficienza dello sviluppo.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Restituisce`VERO` se il controllo è un[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public bool IsForms2OleControl { get; }
```

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

* class [OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
