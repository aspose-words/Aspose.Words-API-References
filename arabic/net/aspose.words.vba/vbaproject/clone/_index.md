---
title: VbaProject.Clone
second_title: Aspose.Words لمراجع .NET API
description: VbaProject طريقة. يقوم بتنفيذ نسخة من ملفVbaProject .
type: docs
weight: 70
url: /ar/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

يقوم بتنفيذ نسخة من ملف[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### قيمة الإرجاع

VbaProject المستنسخ.

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

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbaproject/)
* المجسم [Aspose.Words](../../../)


