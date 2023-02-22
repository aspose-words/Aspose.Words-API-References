---
title: Class ViewOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.ViewOptions فصل. يوفر خيارات متنوعة تتحكم في كيفية عرض المستند في Microsoft Word.
type: docs
weight: 5650
url: /ar/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

يوفر خيارات متنوعة تتحكم في كيفية عرض المستند في Microsoft Word.

```csharp
public class ViewOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | إيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | يحدد ما إذا كان المستند في وضع تصميم النماذج. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | يتحكم في وضع العرض في Microsoft Word . |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | الحصول على أو تعيين النسبة المئوية (بين 10 و 500) التي تريد عرض المستند بها. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | الحصول على قيمة تكبير / تصغير أو تعيينها بناءً على حجم النافذة. |

### أمثلة

يوضح كيفية تعيين عامل تكبير مخصص ، أي الإصدارات القديمة من Microsoft Word سيتم تطبيقها على مستند عند التحميل.

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

يوضح كيفية تعيين نوع تكبير مخصص ، أي الإصدارات القديمة من Microsoft Word سيتم تطبيقها على مستند عند التحميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بتعيين خاصية "ZoomType" على "ZoomType.PageWidth" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليلائم عرض الصفحة.
// قم بتعيين خاصية "ZoomType" على "ZoomType.FullPage" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لجعل الصفحة الأولى بأكملها مرئية.
// قم بتعيين خاصية "ZoomType" على "ZoomType.TextFit" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لملاءمة هوامش النص الداخلية للصفحة الأولى.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### أنظر أيضا

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


