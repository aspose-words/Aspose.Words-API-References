---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ CommandButtonControl. أنشئ أزرارًا وخصّصها بسهولة لتطبيقاتك باستخدام هذه النسخة الفعّالة من الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

يقوم بتهيئة مثيل جديد لـ[`CommandButtonControl`](../) الصف.

```csharp
public CommandButtonControl()
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

* class [CommandButtonControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
