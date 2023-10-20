---
title: Forms2OleControl.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words für .NET
description: Forms2OleControl Value eigendom. Ruft die zugrunde liegende ValueEigenschaft ab die häufig den Steuerungsstatus darstellt. Beispielsweise hat die aktivierte Optionsschaltfläche den Wert 1 während die deaktivierte Option 0 hat. Der Standardwert ist eine leere Zeichenfolge in C#.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Ruft die zugrunde liegende Value-Eigenschaft ab, die häufig den Steuerungsstatus darstellt. Beispielsweise hat die aktivierte Optionsschaltfläche den Wert „1“, während die deaktivierte Option „0“ hat. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string Value { get; }
```

## Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Beachten Sie, dass Sie GroupName nicht für einen Frame festlegen können.
    checkBox.GroupName = "Aspose group name";
}
```

### Siehe auch

* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
