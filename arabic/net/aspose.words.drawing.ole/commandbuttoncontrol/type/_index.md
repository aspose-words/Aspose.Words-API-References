---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CommandButtonControl Type للوصول بسهولة إلى أنواع عناصر التحكم في Forms 2.0، مما يعزز وظائف تطبيقك وتجربة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

يحصل على نوع عنصر التحكم في النماذج 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## أمثلة

يوضح كيفية إدراج عنصر التحكم ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### أنظر أيضا

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
