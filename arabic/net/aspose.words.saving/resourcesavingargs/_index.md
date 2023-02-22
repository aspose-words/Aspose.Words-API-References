---
title: Class ResourceSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.ResourceSavingArgs فصل. توفير بيانات لملفResourceSaving الحدث .
type: docs
weight: 5280
url: /ar/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

توفير بيانات لملف[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) الحدث .

```csharp
public class ResourceSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | الحصول على كائن المستند الذي يتم حفظه حاليًا. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ أحد الموارد. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ المورد فيه. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | الحصول على أو تعيين معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه. |

### ملاحظات

بشكل افتراضي ، عندما يقوم Aspose.Words بحفظ مستند إلى HTML أو SVG بصفحة ثابتة ، فإنه يحفظ كل مورد في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل مورد موجود في المستند.

`ResourceSavingArgs` يسمح بإعادة تعريف كيفية إنشاء أسماء ملفات الموارد أو التحايل تمامًا على حفظ الموارد في الملفات من خلال توفير كائنات الدفق الخاصة بك.

لتطبيق منطقك الخاص لتوليد أسماء ملفات الموارد ، استخدم [`ResourceFileName`](./resourcefilename/) منشأه.

لحفظ الموارد في التدفقات بدلاً من الملفات ، استخدم ملحق[`ResourceStream`](./resourcestream/) منشأه.

### أمثلة

يوضح كيفية استخدام رد الاتصال لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

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
    /// يتم الاستدعاء عندما يحفظ Aspose.Words موردًا خارجيًا لصفحة ثابتة HTML أو SVG.
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


