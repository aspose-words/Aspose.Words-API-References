---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words für .NET
description: Entdecken Sie die CheckBoxControl-Eigenschaft „Checked“ und verwalten Sie Kontrollkästchenzustände ganz einfach mit einem einfachen Booleschen Wert. Der Standardwert ist „false“ für optimale Kontrolle.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Ruft einen booleschen Wert ab oder setzt ihn, der entweder dies angibt[`CheckBoxControl`](../) aktiviert ist oder nicht. Der Standardwert ist`FALSCH` .

```csharp
public bool Checked { get; set; }
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

* class [CheckBoxControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
