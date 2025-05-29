---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CheckBoxControl Checked, hantera enkelt kryssrutestatus med ett enkelt booleskt värde. Standardvärdet är falskt för optimal kontroll.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Hämtar eller ställer in ett booleskt värde som indikerar antingen detta[`CheckBoxControl`](../) är markerad eller inte. Standardvärdet är`falsk` .

```csharp
public bool Checked { get; set; }
```

## Exempel

Visar hur man ändrar status för CheckBox-kontrollen.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Se även

* class [CheckBoxControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
