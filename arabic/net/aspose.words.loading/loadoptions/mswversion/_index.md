---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words لـ .NET
description: حسّن تحميل المستندات باستخدام LoadOptions MswVersion. تأكد من التوافق مع إصدارات MS Word المحددة، مع اختيار Word 2019 افتراضيًا لضمان تكامل سلس.
type: docs
weight: 100
url: /ar/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار MS Word محدد. القيمة الافتراضية هيWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## ملاحظات

قد تتعامل إصدارات Word المختلفة مع جوانب معينة من محتوى المستند وتنسيقه بشكل مختلف قليلاً أثناء عملية التحميل، مما قد يؤدي إلى اختلافات طفيفة في نموذج كائن المستند.

## أمثلة

يوضح كيفية محاكاة إجراء تحميل إصدار معين من Microsoft Word أثناء تحميل المستند.

```csharp
// بشكل افتراضي، يقوم Aspose.Words بتحميل المستندات وفقًا لمواصفات Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// هذه الوثيقة تفتقر إلى نمط تنسيق الفقرة الافتراضي.
// سيتم إعادة إنشاء هذا النمط الافتراضي عندما نقوم بتحميل المستند باستخدام Microsoft Word أو Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// سيكون تباعد أسطر النمط بهذه القيمة عند تحميله بواسطة مواصفات Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### أنظر أيضا

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
