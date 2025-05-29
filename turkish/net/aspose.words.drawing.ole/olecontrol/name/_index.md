---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: ActiveX denetiminizin adını kolayca yönetmek için OleControl Name özelliğini keşfedin. İşlevselliği geliştirin ve geliştirme sürecinizi bugün hızlandırın!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

ActiveX denetiminin adını alır veya ayarlar.

```csharp
public string Name { get; set; }
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

* class [OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
