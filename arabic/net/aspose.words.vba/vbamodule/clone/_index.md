---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: انسخ وحدة VbaModule بسهولة باستخدام طريقة الاستنساخ. بسّط عملية البرمجة لديك وحسّن إنتاجيتك مع هذه الميزة الفعّالة.
type: docs
weight: 50
url: /ar/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

يقوم بإجراء نسخة من[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### قيمة الإرجاع

المستنسخة[`VbaModule`](../).

## أمثلة

يوضح كيفية استنساخ مشروع ووحدة VBA بشكل عميق.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// في المستند الوجهة، لدينا بالفعل وحدة تسمى "Module1"
// لأننا استنسخناها مع المشروع. سنحتاج إلى إزالة الوحدة.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### أنظر أيضا

* class [VbaModule](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
