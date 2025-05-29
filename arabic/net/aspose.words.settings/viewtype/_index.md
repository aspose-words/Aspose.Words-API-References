---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Settings.ViewType enum لبرنامج Microsoft Word. تمتع بأنماط عرض مرنة لتحسين عرض المستندات وتجربة المستخدم.
type: docs
weight: 6790
url: /ar/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

القيم الممكنة لوضع العرض في Microsoft Word.

```csharp
public enum ViewType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | سيتم عرض المستند في العرض الافتراضي للتطبيق. |
| Reading | `0` | سيتم عرض المستند في العرض الافتراضي للتطبيق. |
| PageLayout | `1` | سيتم فتح المستند في عرض يعرض المستند كما سيتم طباعته. |
| Outline | `3` | يجب عرض المستند في عرض مُحسَّن لتحديد الخطوط العريضة أو إنشاء مستندات طويلة. |
| Normal | `4` | يجب عرض المستند في عرض مُحسَّن لتحديد الخطوط العريضة أو إنشاء مستندات طويلة. |
| Web | `5` | سيتم عرض المستند في عرض يحاكي الطريقة التي سيتم بها عرض هذا المستند في صفحة الويب. |

## أمثلة

يوضح كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند تحميله.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### أنظر أيضا

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
