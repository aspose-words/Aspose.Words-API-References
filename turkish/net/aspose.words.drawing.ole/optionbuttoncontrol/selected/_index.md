---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: .NET için Aspose.Words
description: OptionButtonControl'ünüzü kolayca yönetin! Sorunsuz kullanıcı etkileşimi için basit bir boolean değeriyle seçili durumunu ayarlayın veya alın.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Bu değeri belirten bir Boole değeri alır veya ayarlar[`OptionButtonControl`](../) seçilip seçilmediğini.

```csharp
public bool Selected { get; set; }
```

## Notlar

Bu özelliğin, bir gruptaki birden fazla öğeyi seçmenize olanak tanıdığını unutmayın.[`OptionButtonControl`](../) aynı şekilde[`GroupName`](../../forms2olecontrol/groupname/) Bunu yaptığınızda daha önce seçilmiş bir öğenin seçimini kaldırmak sizin sorumluluğunuzdadır.[`OptionButtonControl`](../) seçili.

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

* class [OptionButtonControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
