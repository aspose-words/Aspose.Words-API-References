---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ResourceSavingArgs ResourceFileUri لإدارة ملفات الموارد والرجوع إليها بسهولة في مستنداتك. حسّن كفاءتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

يحصل على معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف الموارد من المستند أو يعينه.

```csharp
public string ResourceFileUri { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية تغيير عناوين URI الخاصة بملفات الموارد المصدرة إلى مستندات HTML أو SVG ذات الصفحات الثابتة.

يُنشئ Aspose.Words تلقائيًا مُعرّف موارد (URI) لكل ملف مورد أثناء التصدير إلى تنسيق HTML لصفحة ثابتة أو SVG. تُشير مُعرّفات الموارد المُولّدة إلى ملفات الموارد المحفوظة بواسطة Aspose.Words. مع ذلك، قد تكون مُعرّفات الموارد (URIs) غير صحيحة إذا كان من المقرر نقل ملفات الموارد إلى موقع آخر أو إذا تم حفظها في تدفقات. تسمح هذه الخاصية بتصحيح مُعرّفات الموارد (URIs) في هذه الحالات.

عند تشغيل الحدث، تحتوي هذه الخاصية على مُعرِّف الموارد المُولَّد بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لتوفير مُعرِّف موارد مُخصَّص لملف الموارد.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
