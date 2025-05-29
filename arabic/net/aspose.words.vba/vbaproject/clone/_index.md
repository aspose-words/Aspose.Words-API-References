---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: انسخ مشروع VbaProject الخاص بك بسهولة باستخدام طريقة الاستنساخ. حسّن سير عملك وحسّن إدارة مشاريعك اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

يقوم بإجراء نسخة من[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### قيمة الإرجاع

المستنسخة[`VbaProject`](../).

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

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
