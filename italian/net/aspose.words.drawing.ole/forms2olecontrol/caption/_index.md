---
title: Forms2OleControl.Caption
second_title: Aspose.Words per .NET API Reference
description: Forms2OleControl proprietà. Ottiene la proprietà Caption del controllo. Il valore predefinito è una stringa vuota.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Ottiene la proprietà Caption del controllo. Il valore predefinito è una stringa vuota.

```csharp
public string Caption { get; }
```

### Esempi

Mostra come verificare le proprietà di un controllo ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### Guarda anche

* class [Forms2OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* assemblea [Aspose.Words](../../../)


