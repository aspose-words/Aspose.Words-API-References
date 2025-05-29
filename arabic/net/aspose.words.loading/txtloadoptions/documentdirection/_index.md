---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TxtLoadOptions DocumentDirection لضبط اتجاه المستند بسهولة. حسّن تخطيطك باستخدام الإعداد الافتراضي "من اليسار إلى اليمين"!
type: docs
weight: 50
url: /ar/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

يحصل على اتجاه المستند أو يعينه. القيمة الافتراضية هيLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## أمثلة

يوضح كيفية اكتشاف اتجاه نص المستند النصي العادي.

```csharp
// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى منشئ المستند
// لتعديل كيفية تحميل مستند النص العادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// تعيين خاصية "DocumentDirection" إلى "DocumentDirection.Auto" يكتشف تلقائيًا
//اتجاه كل فقرة من النص الذي يقوم Aspose.Words بتحميله من النص العادي.
// ستقوم خاصية "Bidi" الخاصة بكل فقرة بتخزين اتجاهها.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// اكتشاف النص العبري من اليمين إلى اليسار.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// اكتشاف النص الإنجليزي من اليمين إلى اليسار.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### أنظر أيضا

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
