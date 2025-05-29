---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.ResourceSavingArgs، التي تعمل على تحسين معالجة المستندات من خلال توفير البيانات الأساسية لحدث ResourceSaving.
type: docs
weight: 6360
url: /ar/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

يوفر بيانات لـ[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) الحدث.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class ResourceSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | يحصل على كائن المستند الذي يتم حفظه حاليًا. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ مورد. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | يحصل على اسم الملف (بدون مسار) الذي سيتم حفظ المورد فيه أو يعينه. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | يحصل على معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف الموارد من المستند أو يعينه. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه. |

## ملاحظات

افتراضيًا، عندما يحفظ Aspose.Words مستندًا بتنسيق HTML أو SVG ثابت الصفحة، فإنه يحفظ كل مورد في ملف منفصل باسم . يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد باسم لكل مورد موجود في المستند.

`ResourceSavingArgs` يسمح بإعادة تعريف كيفية إنشاء أسماء ملفات الموارد أو للالتفاف بشكل كامل على حفظ الموارد في الملفات من خلال توفير كائنات التدفق الخاصة بك.

لتطبيق المنطق الخاص بك لتوليد أسماء ملفات الموارد، استخدم [`ResourceFileName`](./resourcefilename/) ملكية.

لحفظ الموارد في التدفقات بدلاً من الملفات، استخدم[`ResourceStream`](./resourcestream/) ملكية.

## أمثلة

يوضح كيفية استخدام معاودة الاتصال لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// يتم استدعاؤها عندما يقوم Aspose.Words بحفظ مورد خارجي في صفحة ثابتة بتنسيق HTML أو SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
