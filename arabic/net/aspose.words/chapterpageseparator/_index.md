---
title: Enum ChapterPageSeparator
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.ChapterPageSeparator تعداد. تحديد الحرف الفاصل الذي يظهر بين رقم الفصل والصفحة.
type: docs
weight: 200
url: /ar/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

تحديد الحرف الفاصل الذي يظهر بين رقم الفصل والصفحة.

```csharp
public enum ChapterPageSeparator
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Hyphen | `0` | نقطتان. |
| Period | `1` | فترة. |
| Colon | `2` | نقطتان. |
| EmDash | `3` | شرطة مشددة. |
| EnDash | `4` | شرطة قياسية. |

### أمثلة

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


