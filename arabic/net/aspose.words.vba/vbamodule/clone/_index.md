---
title: VbaModule.Clone
second_title: Aspose.Words لمراجع .NET API
description: VbaModule طريقة. يقوم بتنفيذ نسخة من ملفVbaModule .
type: docs
weight: 50
url: /ar/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

يقوم بتنفيذ نسخة من ملف[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### قيمة الإرجاع

النسخة المستنسخة VbaModule.

### أمثلة

يوضح كيفية النسخ العميق لمشروع ووحدة VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// في المستند الوجهة ، لدينا بالفعل وحدة باسم "Module1"
// لأننا استنسخناها مع المشروع. سنحتاج إلى إزالة الوحدة.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### أنظر أيضا

* class [VbaModule](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodule/)
* المجسم [Aspose.Words](../../../)


