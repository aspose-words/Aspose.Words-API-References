---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words لـ .NET
description: PageSetup HeadingLevelForChapter ملكية. الحصول على أو تعيين نمط مستوى العنوان الذي يتم تطبيقه على عناوين الفصول في المستند في C#.
type: docs
weight: 180
url: /ar/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

الحصول على أو تعيين نمط مستوى العنوان الذي يتم تطبيقه على عناوين الفصول في المستند.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## ملاحظات

يمكن أن يكون رقمًا من 0 إلى 9. 0 يعني عدم وجود رقم الفصل إذا تم تطبيقه على رقم الصفحة.

قبل أن تتمكن من إنشاء أرقام الصفحات التي تتضمن أرقام الفصول، يجب أن يكون لعناوين المستند تنسيق مخطط تفصيلي مرقّم مطبق.

## أمثلة

يوضح كيفية العمل مع فصول الصفحة.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
