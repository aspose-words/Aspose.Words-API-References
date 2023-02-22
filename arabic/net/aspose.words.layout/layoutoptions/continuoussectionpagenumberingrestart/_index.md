---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Aspose.Words لمراجع .NET API
description: LayoutOptions ملكية. الحصول على أو تعيين وضع السلوك لحساب أرقام الصفحات عندما يقوم قسم مستمر بإعادة تشغيل ترقيم الصفحات .
type: docs
weight: 40
url: /ar/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

الحصول على أو تعيين وضع السلوك لحساب أرقام الصفحات عندما يقوم قسم مستمر بإعادة تشغيل ترقيم الصفحات .

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### ملاحظات

القيمة الافتراضية هيAlways . إنه يطابق سلوك MS Word 2019 الذي كان أحدث إصدار في الوقت الحالي تم تقديم الخيار . يتوفر منطق ترقيم الصفحات الأقدم الموضح بواسطة MS Word 2016 عبر هذا الخيار . من فضلك[`ContinuousSectionRestart`](../../continuoussectionrestart/) لوصف السلوك.

### أمثلة

يوضح كيفية التحكم في ترقيم الصفحات في قسم مستمر.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// افتراضيًا ، يتطابق سلوك Aspose.Words مع Microsoft Word 2019.
// إذا كنت بحاجة إلى سلوك Aspose.Words القديم ، Microsoft Word 2016 المتكرر ، استخدم "ContinuousSectionRestart.FromNewPageOnly".
// يتم إعادة تشغيل ترقيم الصفحات فقط إذا لم يكن هناك محتوى آخر قبل القسم الموجود على الصفحة حيث يبدأ القسم ،
// بسبب ذلك سيتم إعادة تعيين الترقيم إلى 2 من الصفحة الثانية.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### أنظر أيضا

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../layoutoptions/)
* المجسم [Aspose.Words](../../../)


