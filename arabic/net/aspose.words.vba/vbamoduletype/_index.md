---
title: Enum VbaModuleType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Vba.VbaModuleType تعداد. يحدد نوع النموذج في مشروع VBA.
type: docs
weight: 6570
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
| DocumentModule | `0` | نوع من عناصر مشروع VBA يحدد وحدة نمطية لوحدات الماكرو المضمنة وعمليات الوصول البرمجي المرتبطة بالمستند. |
| ProceduralModule | `1` | مجموعة من الإجراءات الفرعية والوظائف. |
| ClassModule | `2` | وحدة تحتوي على تعريف كائن جديد. يقوم كل مثيل لفئة بإنشاء كائن جديد، وتصبح الإجراءات التي تم تحديدها في الوحدة خصائص وأساليب للكائن. |
| DesignerModule | `3` | وحدة VBA التي تعمل على توسيع أساليب وخصائص عنصر تحكم ActiveX الذي تم تسجيله في المشروع. |

### أمثلة

يوضح كيفية إنشاء مشروع VBA باستخدام وحدات الماكرو.

```csharp
Document doc = new Document();

// إنشاء مشروع VBA جديد.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// أنشئ وحدة نمطية جديدة وحدد كود مصدر الماكرو.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// أضف الوحدة النمطية إلى مشروع VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)


