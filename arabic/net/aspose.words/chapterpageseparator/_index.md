---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.ChapterPageSeparator لتخصيص فواصل أرقام الفصول والصفحات لتحسين تنسيق المستندات ووضوحها.
type: docs
weight: 390
url: /ar/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

يحدد حرف الفاصل الذي يظهر بين الفصل ورقم الصفحة.

```csharp
public enum ChapterPageSeparator
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Hyphen | `0` | نقطتان. |
| Period | `1` | فترة. |
| Colon | `2` | نقطتان. |
| EmDash | `3` | شرطة مُؤكدة. |
| EnDash | `4` | شرطة قياسية. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
