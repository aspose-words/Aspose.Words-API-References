---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die CheckBoxControl-Typ-Eigenschaft für Forms 2.0 und schalten Sie vielseitige Steuerungsoptionen frei, um die Funktionalität Ihrer Anwendung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

Ruft den Typ des Forms 2.0-Steuerelements ab.

```csharp
public override Forms2OleControlType Type { get; }
```

## Beispiele

Zeigt, wie der Status des CheckBox-Steuerelements geändert wird.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Siehe auch

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
