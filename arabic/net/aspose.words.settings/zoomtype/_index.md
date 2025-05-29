---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Settings.ZoomType enum لتخصيص أحجام عرض المستندات في Microsoft Word للحصول على عرض وإنتاجية مثالية.
type: docs
weight: 6810
url: /ar/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

القيم المحتملة لحجم المستند الذي يظهر على الشاشة في Microsoft Word.

```csharp
public enum ZoomType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Custom | `0` | تم تعيين نسبة التكبير/التصغير بشكل صريح. لا يُعاد حسابها تلقائيًا عند تغيير حجم عنصر التحكم. |
| None | `0` | يشير إلى استخدام نسبة التكبير/التصغير الصريحة. نفسCustom . |
| FullPage | `1` | يتم إعادة حساب نسبة التكبير تلقائيًا لتناسب صفحة كاملة. |
| PageWidth | `2` | يتم إعادة حساب نسبة التكبير تلقائيًا لتناسب عرض الصفحة. |
| TextFit | `3` | يتم إعادة حساب نسبة التكبير تلقائيًا لتناسب النص. |

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
* property [ZoomType](../viewoptions/zoomtype/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
