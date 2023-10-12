---
title: ViewOptions.ZoomPercent
second_title: Aspose.Words لمراجع .NET API
description: ViewOptions ملكية. الحصول على أو تعيين النسبة المئوية بين 10 و500 التي تريد عرض مستندك بها.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

الحصول على أو تعيين النسبة المئوية (بين 10 و500) التي تريد عرض مستندك بها.

```csharp
public int ZoomPercent { get; set; }
```

### ملاحظات

إذا كانت القيمة 0، فإن هذه الخاصية تستخدم 100 بدلاً من ذلك، وإلا إذا كانت القيمة أقل من 10 أو أكبر من 500، فستطرح هذه الخاصية.

على الرغم من أن Aspose.Words قادر على قراءة هذا الخيار وكتابته، إلا أن استخدامه خاص بالتطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

### أمثلة

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

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../viewoptions/)
* المجسم [Aspose.Words](../../../)


