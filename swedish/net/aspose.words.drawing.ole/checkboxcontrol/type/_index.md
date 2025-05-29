---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CheckBoxControl Type för Forms 2.0, som låser upp mångsidiga kontrollalternativ för att förbättra programmets funktionalitet.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

Hämtar typ av Forms 2.0-kontroll.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
