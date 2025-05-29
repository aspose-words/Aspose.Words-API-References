---
title: Forms2OleControl.ChildNodes
linktitle: ChildNodes
articleTitle: ChildNodes
second_title: .NET için Aspose.Words
description: Gelişmiş işlevsellik için anında alt denetimlere zahmetsizce erişmek ve bunları yönetmek amacıyla Forms2OleControl ChildNodes özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Hemen alt kontrollerin koleksiyonunu alır.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

## Notlar

İade`hükümsüz` eğer bu kontrol çocuk sahibi olamazsa.

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

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
