---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words لـ .NET
description: استكشف قائمة Aspose.Words.Layout.ContinuousSectionRestart لترقيم الصفحات بمرونة في الأقسام المتصلة. حسّن تخطيط المستند بسهولة!
type: docs
weight: 3750
url: /ar/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد تشغيل ترقيم الصفحات.

```csharp
public enum ContinuousSectionRestart
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Always | `0` | يتم إعادة تشغيل ترقيم الصفحات دائمًا بغض النظر عن تدفق المحتوى. |
| FromNewPageOnly | `1` | يتم إعادة تشغيل ترقيم الصفحات فقط إذا لم يكن هناك أي محتوى آخر قبل القسم في الصفحة التي يبدأ فيها القسم. |

## أمثلة

يوضح كيفية التحكم في ترقيم الصفحات في قسم مستمر.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// بشكل افتراضي، يتطابق سلوك Aspose.Words مع سلوك Microsoft Word 2019.
// إذا كنت بحاجة إلى سلوك Aspose.Words القديم، وتكرار Microsoft Word 2016، استخدم 'ContinuousSectionRestart.FromNewPageOnly'.
// يتم إعادة تشغيل ترقيم الصفحات فقط إذا لم يكن هناك أي محتوى آخر قبل القسم الموجود في الصفحة حيث يبدأ القسم،
// وبسبب ذلك سيتم إعادة تعيين الترقيم إلى 2 من الصفحة الثانية.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
