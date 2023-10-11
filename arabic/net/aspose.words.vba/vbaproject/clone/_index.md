---
title: VbaProject.Clone
second_title: Aspose.Words لمراجع .NET API
description: VbaProject طريقة. ينفذ نسخة منVbaProject .
type: docs
weight: 70
url: /ar/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

ينفذ نسخة من[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### قيمة الإرجاع

المستنسخة[`VbaProject`](../).

### أمثلة

يوضح كيفية الاستنساخ العميق لمشروع ووحدة VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// في المستند الوجهة، لدينا بالفعل وحدة تسمى "Module1"
// لأننا قمنا باستنساخه مع المشروع. سنحتاج إلى إزالة الوحدة.
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


