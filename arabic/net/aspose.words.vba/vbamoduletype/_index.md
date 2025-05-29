---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Vba.VbaModuleType enum، الذي يحدد أنواع النماذج في مشاريع VBA لتحسين الأتمتة وإدارة المستندات بشكل مبسط.
type: docs
weight: 7420
url: /ar/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

يحدد نوع النموذج في مشروع VBA.

```csharp
public enum VbaModuleType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| DocumentModule | `0` | نوع من عناصر مشروع VBA يحدد وحدة للماكرو المضمنة وعمليات الوصول البرمجية المرتبطة بمستند. |
| ProceduralModule | `1` | مجموعة من البرامج الفرعية والوظائف. |
| ClassModule | `2` | وحدة تحتوي على تعريف كائن جديد. كل مثيل للفئة يُنشئ كائنًا جديدًا، ، والإجراءات المُعرّفة في الوحدة تُصبح خصائص وطرقًا للكائن. |
| DesignerModule | `3` | وحدة VBA تعمل على توسيع الأساليب وخصائص عنصر تحكم ActiveX الذي تم تسجيله مع المشروع. |

## أمثلة

يوضح كيفية إنشاء مشروع VBA باستخدام وحدات الماكرو.

```csharp
Document doc = new Document();

// إنشاء مشروع VBA جديد.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// قم بإنشاء وحدة نمطية جديدة وحدد كود مصدر الماكرو.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

//أضف الوحدة إلى مشروع VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
