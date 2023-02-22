---
title: OleFormat.OleControl
second_title: Aspose.Words for .NET API Referansı
description: OleFormat mülk. AlırOleControl Bu OLE nesnesi bir ActiveX denetimiyse nesneler. Aksi takdirde bu özellik null. olur.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Alır`OleControl` Bu OLE nesnesi bir ActiveX denetimiyse, nesneler. Aksi takdirde bu özellik null. olur.

```csharp
public OleControl OleControl { get; }
```

### Örnekler

ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

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

### Ayrıca bakınız

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../oleformat/)
* toplantı [Aspose.Words](../../../)


