---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: .NET için Aspose.Words
description: ActiveX denetim nesnelerine erişmek için OleFormat OleControl özelliğini keşfedin. OLE uygulamalarınız için gelişmiş işlevselliğin ve entegrasyonun kilidini açın.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Alır`OleControl` Bu OLE nesnesi bir ActiveX denetimiyse nesneler. Aksi takdirde bu özellik null'dır.

```csharp
public OleControl OleControl { get; }
```

## Örnekler

Bir ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

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

    // Bir Çerçeve için GrupAdı ayarlayamayacağınızı unutmayın.
    checkBox.GroupName = "Aspose group name";
}
```

### Ayrıca bakınız

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
