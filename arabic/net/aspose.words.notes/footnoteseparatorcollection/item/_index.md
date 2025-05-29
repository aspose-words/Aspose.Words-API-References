---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى خاصية عنصر FootnoteSeparatorCollection لاسترداد FootnoteSeparators المخصصة حسب النوع بسهولة، مما يؤدي إلى تحسين تنسيق مستندك.
type: docs
weight: 20
url: /ar/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

يسترجع[`FootnoteSeparator`](../../footnoteseparator/) من النوع المحدد.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## ملاحظات

إرجاع`باطل` إذا لم يتم العثور على فاصل الحاشية السفلية/الحاشية النهائية للنوع المحدد.

## أمثلة

يوضح كيفية إدارة تنسيق فاصل الحاشية السفلية.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
//محاذاة فاصل الحاشية السفلية.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### أنظر أيضا

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
