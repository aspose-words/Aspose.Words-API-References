---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى فواصل الحواشي السفلية والختامية وتخصيصها في مستندك باستخدام خاصية FootnoteSeparators في DocumentBase لتحسين التحكم في التنسيق.
type: docs
weight: 40
url: /ar/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

يوفر الوصول إلى فواصل الحواشي السفلية/النهائية المحددة في المستند.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

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

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
