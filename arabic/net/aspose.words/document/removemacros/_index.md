---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words لـ .NET
description: قم بإزالة جميع وحدات الماكرو وأشرطة الأدوات وإعدادات الأوامر المخصصة من مشروع VBA الخاص بك بسهولة باستخدام طريقة Document RemoveMacros للحصول على مستند أنظف.
type: docs
weight: 720
url: /ar/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

يزيل جميع وحدات الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند.

```csharp
public void RemoveMacros()
```

## ملاحظات

من خلال إزالة كافة وحدات الماكرو من المستند، يمكنك التأكد من أن المستند لا يحتوي على فيروسات ماكرو.

## أمثلة

يوضح كيفية إزالة كافة وحدات الماكرو من مستند.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// قم بإزالة مشروع VBA الخاص بالمستند، مع كل وحدات الماكرو الخاصة به.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
