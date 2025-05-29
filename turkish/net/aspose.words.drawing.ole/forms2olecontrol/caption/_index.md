---
title: Forms2OleControl.Caption
linktitle: Caption
articleTitle: Caption
second_title: .NET için Aspose.Words
description: Denetiminizin başlığını kolayca özelleştirmek için Forms2OleControl Caption özelliğini keşfedin. Bu basit ve etkili özellik ile kullanıcı deneyimini geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Denetimin Başlık özelliğini alır veya ayarlar. Varsayılan değer boş bir dizedir.

```csharp
public string Caption { get; set; }
```

## Örnekler

ActiveX denetimi için başlığın nasıl ayarlanacağını gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl() { Caption = "Button caption" };
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual("Button caption", button1.Caption);
```

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

* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
