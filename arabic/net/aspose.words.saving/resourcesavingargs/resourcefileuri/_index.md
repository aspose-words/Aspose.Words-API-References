---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words لـ .NET
description: ResourceSavingArgs ResourceFileUri ملكية. الحصول على أو تعيين معرف المورد الموحد URI المستخدم للإشارة إلى ملف المورد من المستند في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

الحصول على أو تعيين معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند.

```csharp
public string ResourceFileUri { get; set; }
```

## ملاحظات

تسمح لك هذه الخاصية بتغيير معرفات URI لملفات الموارد المصدرة إلى مستندات HTML أو SVG ذات صفحة ثابتة.

يقوم Aspose.Words تلقائيًا بإنشاء URI لكل ملف مورد أثناء التصدير إلى صفحة ثابتة بتنسيق HTML أو SVG. تشير معرفات URI التي تم إنشاؤها إلى ملفات الموارد المحفوظة بواسطة Aspose.Words. ومع ذلك، يمكن أن تكون عناوين URI غير صحيحة إذا تم نقل ملفات الموارد إلى موقع آخر أو إذا تم حفظ ملفات الموارد في التدفقات. تسمح هذه الخاصية بتصحيح معرفات URI في هذه الحالات.

عند إطلاق الحدث، تحتوي هذه الخاصية على URI الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لتوفير عنوان URI مخصص لملف المورد.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
