---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup HeadingLevelForChapter لتخصيص أنماط عناوين الفصول بسهولة في مستندك لتحسين قابلية القراءة والاحترافية.
type: docs
weight: 180
url: /ar/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

يحصل على نمط مستوى العنوان المطبق على عناوين الفصول في المستند أو يعينه.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## ملاحظات

يمكن أن يكون رقمًا من 0 إلى 9. 0 يعني عدم وجود رقم الفصل إذا تم تطبيقه على رقم الصفحة.

قبل أن تتمكن من إنشاء أرقام الصفحات التي تتضمن أرقام الفصول، يجب تطبيق تنسيق مخطط مرقم على عناوين المستندات.

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
