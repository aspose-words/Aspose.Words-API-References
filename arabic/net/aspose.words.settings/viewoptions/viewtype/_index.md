---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words لـ .NET
description: ViewOptions ViewType ملكية. يتحكم في وضع العرض في Microsoft Word في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

يتحكم في وضع العرض في Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## ملاحظات

على الرغم من أن Aspose.Words قادر على قراءة هذا الخيار وكتابته، إلا أن استخدامه خاص بالتطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

## أمثلة

يوضح كيفية تعيين عامل تكبير مخصص، أي الإصدارات الأقدم من Microsoft Word سيتم تطبيقها على المستند عند التحميل.

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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
