---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words لـ .NET
description: حسّن حفظ EMF باستخدام ImageSaveOptions. تحكّم في إعدادات مُقدّم GDI أو Aspose.Words لتحسين جودة الصورة وأدائها.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استخدام GDI+ أو Aspose.Words metafile renderer عند الحفظ في EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## ملاحظات

إذا تم ضبطه على`حقيقي` يُستخدم مُقدِّم ملفات تعريف GDI+. أي أنه يُكتب المحتوى إلى كائن GDI+ graphics ويُحفظ في ملف تعريف.

إذا تم ضبطه على`خطأ شنيع` يُستخدم مُقدِّم ملفات التعريف Aspose.Words. أي أنه يُكتب المحتوى مباشرةً إلى تنسيق ملف التعريف باستخدام Aspose.Words.

يكون له تأثير فقط عند الحفظ في EMF.

يعمل الحفظ GDI+ فقط على .NET.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية اختيار برنامج العرض عند تحويل مستند إلى .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة EMF، يمكننا تمرير كائن SaveOptions لتحديد برنامج عرض الصورة.
// إذا قمنا بتعيين علامة "UseGdiEmfRenderer" إلى "true"، فسوف يستخدم Aspose.Words برنامج العرض GDI+.
// إذا قمنا بتعيين علامة "UseGdiEmfRenderer" إلى "false"، فسوف يستخدم Aspose.Words برنامج تقديم الملف التعريفي الخاص به.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
