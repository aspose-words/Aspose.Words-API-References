---
title: Clone
second_title: Aspose.Words لمراجع .NET API
description: يقوم بتنفيذ نسخة من ملفVbaModuleaspose.words.vba/vbamodule .
type: docs
weight: 50
url: /ar/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

يقوم بتنفيذ نسخة من ملف[`VbaModule`](../../vbamodule) .

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

* class [VbaModule](../../vbamodule)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodule)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
