---
title: Document.RemoveMacros
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إزالة كافة وحدات الماكرو مشروع VBA بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند.
type: docs
weight: 690
url: /ar/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

إزالة كافة وحدات الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند.

```csharp
public void RemoveMacros()
```

### ملاحظات

عن طريق إزالة كافة وحدات الماكرو من مستند، يمكنك التأكد من أن المستند لا يحتوي على فيروسات ماكرو.

### أمثلة

يوضح كيفية إزالة كافة وحدات الماكرو من مستند.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// قم بإزالة مشروع VBA الخاص بالمستند، بالإضافة إلى كافة وحدات الماكرو الخاصة به.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


