---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: .NET için Aspose.Words
description: Forms2OleControl'ü DocumentBuilder'ın InsertForms2OleControl metoduyla zahmetsizce entegre edin. Belge işlevselliğinizi bugün geliştirin!
type: docs
weight: 350
url: /tr/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Ekler[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) nesneyi geçerli konuma taşı.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Geri dönüş değeri

[`Shape`](../../../aspose.words.drawing/shape/) geçeni içeren nesne[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Örnekler

ActiveX denetiminin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ayrıca bakınız

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
