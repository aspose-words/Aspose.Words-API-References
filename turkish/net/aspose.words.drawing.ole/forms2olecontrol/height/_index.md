---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: .NET için Aspose.Words
description: Forms2OleControl'ün yükseklik özelliğini, en iyi görüntüleme ve işlevsellik için noktalar halinde zahmetsizce ayarlayın. Kullanıcı arayüzünüzü hassas kontrol boyutlarıyla geliştirin!
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Kontrolün yüksekliğini noktalar halinde alır veya ayarlar.

```csharp
public double Height { get; set; }
```

## Örnekler

ActiveX denetimi için özelliklerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Ayrıca bakınız

* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
