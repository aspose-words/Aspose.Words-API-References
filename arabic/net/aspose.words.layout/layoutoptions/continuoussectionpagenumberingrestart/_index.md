---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LayoutOptions ContinuousSectionPageNumberingRestart للتحكم السلس في ترقيم الصفحات في الأقسام المتصلة. حسّن تخطيط مستندك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

يحصل على أو يعين وضع السلوك لحساب أرقام الصفحات عندما يقوم القسم المستمر بإعادة تشغيل ترقيم الصفحات.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## ملاحظات

القيمة الافتراضية هيAlways . يتوافق مع سلوك MS Word 2019 وهو الإصدار الأحدث في الوقت الذي تم فيه تقديم الخيار. يتوفر منطق ترقيم الصفحات الأقدم الذي أظهره MS Word 2016 عبر هذا الخيار. من فضلك[`ContinuousSectionRestart`](../../continuoussectionrestart/) لوصف السلوك.

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
