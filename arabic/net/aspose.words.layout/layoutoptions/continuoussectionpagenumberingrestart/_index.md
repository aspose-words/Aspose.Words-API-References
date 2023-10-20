---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words لـ .NET
description: LayoutOptions ContinuousSectionPageNumberingRestart ملكية. الحصول على أو تعيين وضع السلوك لحساب أرقام الصفحات عندما يقوم قسم مستمر بإعادة تشغيل ترقيم الصفحات في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

الحصول على أو تعيين وضع السلوك لحساب أرقام الصفحات عندما يقوم قسم مستمر بإعادة تشغيل ترقيم الصفحات.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## ملاحظات

القيمة الافتراضية هيAlways. إنه يطابق سلوك MS Word 2019 الذي كان الإصدار الأحدث في وقت تقديم الخيار. يتوفر منطق ترقيم الصفحات الأقدم الذي أظهره MS Word 2016 عبر هذا الخيار. من فضلك[`ContinuousSectionRestart`](../../continuoussectionrestart/) لوصف السلوك.

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
