---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: .NET için Aspose.Words
description: Forms2OleControl'ün Genişlik özelliğini noktalar halinde hassas kontrol boyutlandırması için nasıl kolayca ayarlayacağınızı keşfedin. UI tasarımınızı zahmetsizce geliştirin!
type: docs
weight: 100
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Kontrolün genişliğini noktalar halinde alır veya ayarlar.

```csharp
public double Width { get; set; }
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
