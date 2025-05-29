---
title: Forms2OleControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà Type di Forms2OleControl per recuperare facilmente il tipo di controlli Forms 2.0, migliorando così la funzionalità e l'efficienza della tua applicazione.
type: docs
weight: 80
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

Ottiene il tipo di controllo Forms 2.0.

```csharp
public abstract Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
