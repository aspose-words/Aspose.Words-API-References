---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words لـ .NET
description: يمكنك التحكم في استخدام علامات الوصل في مستندك باستخدام خاصية ParagraphFormat SuppressAutoHyphens، مما يضمن تنسيق الفقرة بشكل واضح واحترافي.
type: docs
weight: 380
url: /ar/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

يحدد ما إذا كان يجب إعفاء الفقرة الحالية من أي علامة وصل يتم تطبيقها في إعدادات المستند.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## أمثلة

يوضح كيفية منع استخدام الواصلة في الفقرة.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص بإعدادات محلية تتطابق مع تلك الموجودة في قاموسنا.
// عندما نحفظ هذا المستند بتنسيق حفظ صفحة ثابتة، سيحتوي نصه على علامة الوصل.
Document doc = new Document(MyDir + "German text.docx");

// يمكننا تعيين خاصية "SuppressAutoHyphens" إلى "true" لتعطيل استخدام الواصلة
// لفقرة محددة مع إبقاء ذلك ممكّنًا لبقية المستند.
// القيمة الافتراضية لهذه الخاصية هي "false"،
// وهذا يعني أن كل فقرة تستخدم بشكل افتراضي علامات الوصل إذا كانت متوفرة.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
