---
title: Forms2OleControl.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: .NET için Aspose.Words
description: Kontrolünüzün arka plan rengini özelleştirmek için Forms2OleControl BackColor özelliğini keşfedin. Kullanıcı arayüzünüzü bugün esnek renk seçenekleriyle geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/backcolor/
---
## Forms2OleControl.BackColor property

Denetimin arka plan rengini alır veya ayarlar. Varsayılan değer denetimin türüne bağlıdır.

```csharp
public Color BackColor { get; set; }
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
