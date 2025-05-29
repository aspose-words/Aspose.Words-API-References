---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: .NET için Aspose.Words
description: Kontrolünüzün ön plan rengini kolayca özelleştirmek için Forms2OleControl ForeColor özelliğini keşfedin. Bugün özelleştirilmiş renk seçenekleriyle kullanıcı arayüzünüzü geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

Denetimin ön plan rengini alır veya ayarlar. Varsayılan değer, denetimin türüne bağlıdır.

```csharp
public Color ForeColor { get; set; }
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
