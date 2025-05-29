---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words لـ .NET
description: اضبط خاصية ZoomPercent في ViewOptions لضبط مستوى تكبير مستندك بين ١٠٪ و٥٠٠٪. حسّن سهولة القراءة وحسّن تجربة المشاهدة!
type: docs
weight: 50
url: /ar/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

يحصل على النسبة المئوية التي تريد عرض مستندك بها أو يعينها.

```csharp
public int ZoomPercent { get; set; }
```

## ملاحظات

على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يعتمد على التطبيق. على سبيل المثال، لا يحترم MS Word 2013 قيمة هذا الخيار.

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

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
