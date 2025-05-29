---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Notes.FootnoteSeparatorCollection للوصول بسهولة إلى فواصل الحواشي السفلية في مستنداتك. حسّن تنسيق مستنداتك اليوم!
type: docs
weight: 5000
url: /ar/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

يوفر الوصول المكتوب إلى[`FootnoteSeparator`](../footnoteseparator/) عقد المستند.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | يسترجع[`FootnoteSeparator`](../footnoteseparator/) من النوع المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## أمثلة

يوضح كيفية إدارة تنسيق فاصل الحاشية السفلية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
//محاذاة فاصل الحاشية السفلية.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### أنظر أيضا

* class [FootnoteSeparator](../footnoteseparator/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
