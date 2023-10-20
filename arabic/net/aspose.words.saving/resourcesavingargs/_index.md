---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ResourceSavingArgs فصل. يوفر بيانات لـResourceSaving حدث في C#.
type: docs
weight: 5560
url: /ar/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

يوفر بيانات لـ[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) حدث.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class ResourceSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | الحصول على كائن المستند الذي يتم حفظه حاليًا. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ المورد. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | الحصول على أو تعيين اسم الملف (بدون مسار) حيث سيتم حفظ المورد فيه. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | الحصول على أو تعيين معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه. |

## ملاحظات

افتراضيًا، عندما يقوم Aspose.Words بحفظ مستند في صفحة ثابتة بتنسيق HTML أو SVG، فإنه يحفظ كل مورد في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء ملف name فريد لكل مورد موجود في المستند.

`ResourceSavingArgs` يسمح بإعادة تعريف كيفية إنشاء أسماء ملفات الموارد أو للتحايل تمامًا على حفظ الموارد في الملفات عن طريق توفير كائنات الدفق الخاصة بك.

لتطبيق المنطق الخاص بك لإنشاء أسماء ملفات الموارد، استخدم [`ResourceFileName`](./resourcefilename/) ملكية.

لحفظ الموارد في التدفقات بدلاً من الملفات، استخدم الملف[`ResourceStream`](./resourcestream/) ملكية.

## أمثلة

يوضح كيفية استخدام رد اتصال لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

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
    /// يتم استدعاؤه عندما يقوم Aspose.Words بحفظ مورد خارجي في صفحة ثابتة بتنسيق HTML أو SVG.
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
