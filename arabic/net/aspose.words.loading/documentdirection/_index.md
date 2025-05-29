---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.DocumentDirection للتحكم بسهولة في تدفق النص في مستنداتك. حسّن سهولة القراءة والتنسيق مع هذه الميزة الفعّالة!
type: docs
weight: 4030
url: /ar/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

يسمح بتحديد الاتجاه الذي سيتدفق فيه النص في المستند.

```csharp
public enum DocumentDirection
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| LeftToRight | `0` | الاتجاه من اليسار إلى اليمين. |
| RightToLeft | `1` | الاتجاه من اليمين إلى اليسار. |
| Auto | `2` | اكتشاف الاتجاه تلقائيًا. |

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
