---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.ContinuousSectionRestart تعداد. يمثل سلوكيات مختلفة عند حساب أرقام الصفحات في قسم مستمر يعيد تشغيل ترقيم الصفحات في C#.
type: docs
weight: 3300
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
| Always | `0` | تتم إعادة تشغيل ترقيم الصفحات دائمًا بغض النظر عن تدفق المحتوى. |
| FromNewPageOnly | `1` | تتم إعادة تشغيل ترقيم الصفحات فقط في حالة عدم وجود محتوى آخر قبل القسم الموجود في الصفحة التي يبدأ فيها القسم. |

## أمثلة

يوضح كيفية التحكم في ترقيم الصفحات في قسم مستمر.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// افتراضيًا، يتطابق سلوك Aspose.Words مع Microsoft Word 2019.
// إذا كنت بحاجة إلى سلوك Aspose.Words القديم، أو Microsoft Word 2016 المتكرر، فاستخدم "ContiniousSectionRestart.FromNewPageOnly".
// تتم إعادة تشغيل ترقيم الصفحات فقط في حالة عدم وجود محتوى آخر قبل القسم الموجود في الصفحة التي يبدأ فيها القسم،
// وبسبب ذلك سيتم إعادة تعيين الترقيم إلى 2 من الصفحة الثانية.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
