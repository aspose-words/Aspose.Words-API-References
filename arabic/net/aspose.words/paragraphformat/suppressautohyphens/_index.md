---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. يحدد ما إذا كان ينبغي استثناء الفقرة الحالية من أي وصلة يتم تطبيقها في إعدادات المستند.
type: docs
weight: 370
url: /ar/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

يحدد ما إذا كان ينبغي استثناء الفقرة الحالية من أي وصلة يتم تطبيقها في إعدادات المستند.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### أمثلة

يوضح كيفية منع الواصلة للفقرة.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص ذي لغة محلية مطابقة لتلك الموجودة في قاموسنا.
// عندما نحفظ هذا المستند بتنسيق حفظ صفحة ثابت، سيكون نصه مزودًا بواصلة.
Document doc = new Document(MyDir + "German text.docx");

// يمكننا ضبط خاصية "SuppressAutoHyphens" على "صحيح" لتعطيل الواصلة
// لفقرة معينة مع إبقائها ممكنة لبقية المستند.
// القيمة الافتراضية لهذه الخاصية هي "خطأ"،
// مما يعني أن كل فقرة تستخدم الواصلة بشكل افتراضي، إن وجدت.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


