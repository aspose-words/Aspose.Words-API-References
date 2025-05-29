---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words لـ .NET
description: دمج Forms2OleControl بسهولة مع طريقة InsertForms2OleControl في DocumentBuilder. حسّن أداء مستندك اليوم!
type: docs
weight: 350
url: /ar/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

إدراجات[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) الكائن في الموضع الحالي.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### قيمة الإرجاع

[`Shape`](../../../aspose.words.drawing/shape/) الكائن الذي يحتوي على تمريرة[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## أمثلة

يوضح كيفية إدراج عنصر التحكم ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### أنظر أيضا

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
