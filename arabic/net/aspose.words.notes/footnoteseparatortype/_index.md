---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.FootnoteSeparatorType لتخصيص فواصل الحواشي السفلية والختامية، مما يعزز تنسيق المستند وقابليته للقراءة.
type: docs
weight: 5010
url: /ar/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

يحدد نوع فاصل الحاشية السفلية/النهاية.

```csharp
public enum FootnoteSeparatorType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| FootnoteSeparator | `0` | فاصل بين النص الرئيسي ونص الحاشية السفلية. |
| FootnoteContinuationSeparator | `1` | مطبوع فوق نص الحاشية السفلية على الصفحة عندما يجب متابعة النص من الصفحة السابقة. |
| FootnoteContinuationNotice | `2` | مطبوع أسفل نص الحاشية السفلية على صفحة عندما يجب أن يستمر نص الحاشية السفلية على صفحة لاحقة. |
| EndnoteSeparator | `3` | فاصل بين النص الرئيسي ونص الحاشية الختامية. |
| EndnoteContinuationSeparator | `4` | مطبوع فوق نص الحاشية الختامية في الصفحة عندما يجب متابعة النص من الصفحة السابقة. |
| EndnoteContinuationNotice | `5` | مطبوع أسفل نص الحاشية الختامية على صفحة عندما يجب أن يستمر نص الحاشية الختامية على صفحة لاحقة. |

## أمثلة

يوضح كيفية إزالة فاصل الحاشية الختامية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// إزالة فاصل الحاشية الختامية.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

يوضح كيفية إدارة تنسيق فاصل الحاشية السفلية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
//محاذاة فاصل الحاشية السفلية.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
