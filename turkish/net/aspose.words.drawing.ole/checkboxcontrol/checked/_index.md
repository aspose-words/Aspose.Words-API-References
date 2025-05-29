---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: .NET için Aspose.Words
description: CheckBoxControl Checked özelliğini keşfedin, basit bir boolean değeriyle onay kutusu durumlarını kolayca yönetin. En iyi kontrol için varsayılan değer false'tur.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Bu değeri belirten bir Boole değeri alır veya ayarlar[`CheckBoxControl`](../) işaretli mi değil mi? Varsayılan değer`YANLIŞ` .

```csharp
public bool Checked { get; set; }
```

## Örnekler

CheckBox denetiminin durumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Ayrıca bakınız

* class [CheckBoxControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
