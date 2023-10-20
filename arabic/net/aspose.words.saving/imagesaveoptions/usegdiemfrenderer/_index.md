---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words لـ .NET
description: ImageSaveOptions UseGdiEmfRenderer ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام عارض ملف التعريف GDI أو Aspose.Words عند الحفظ في EMF في C#.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استخدام عارض ملف التعريف GDI+ أو Aspose.Words عند الحفظ في EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## ملاحظات

إذا تم تعيينه على`حقيقي` يتم استخدام عارض ملف التعريف GDI+. أي تتم كتابة المحتوى إلى كائن GDI+ graphics ويتم حفظه في ملف التعريف.

إذا تم تعيينه على`خطأ شنيع` يتم استخدام عارض ملف تعريف Aspose.Words. أي تتم كتابة المحتوى مباشرة إلى تنسيق ملف التعريف باستخدام Aspose.Words.

يكون له تأثير فقط عند الحفظ في EMF.

يعمل حفظ GDI+ على .NET فقط.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية اختيار العارض عند تحويل مستند إلى .emf.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // عندما نحفظ المستند كصورة EMF، يمكننا تمرير كائن SaveOptions لتحديد عارض للصورة.
            // إذا قمنا بتعيين علامة "UseGdiEmfRenderer" على "صحيح"، فسوف يستخدم Aspose.Words عارض GDI+.
            // إذا قمنا بتعيين علامة "UseGdiEmfRenderer" على "خطأ"، فسوف يستخدم Aspose.Words عارض ملف التعريف الخاص به.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // عادةً ما يقوم عارض GDI+ بإنشاء ملفات أكبر.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### أنظر أيضا

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
