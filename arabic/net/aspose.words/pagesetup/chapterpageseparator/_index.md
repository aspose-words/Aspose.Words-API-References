---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChapterPageSeparator في PageSetup. خصّص بسهولة الفاصل بين أرقام الفصول والصفحات لمظهر أنيق.
type: docs
weight: 90
url: /ar/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

يحصل على أو يعين حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## ملاحظات

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
