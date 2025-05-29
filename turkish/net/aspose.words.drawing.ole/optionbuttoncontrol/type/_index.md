---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Forms 2.0 için OptionButtonControl Type özelliğini keşfedin. Formlarınızı bu temel kontrol türü özelliğiyle nasıl geliştirebileceğinizi öğrenin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Forms 2.0 denetiminin türünü alır.

```csharp
public override Forms2OleControlType Type { get; }
```

## Örnekler

Radyo düğmesinin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Seçili ilk öğeyi seçimi kaldır.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// İkinci seçeneği seç butonu.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Ayrıca bakınız

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
