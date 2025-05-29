---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words لـ .NET
description: أدر مواردك بكفاءة مع ResourceSavingArgs. حدّد أو استرجاع اسم الملف لحفظ الموارد بسهولة، دون عناء البحث عن مسارات.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

يحصل على اسم الملف (بدون مسار) الذي سيتم حفظ المورد فيه أو يعينه.

```csharp
public string ResourceFileName { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات الموارد أثناء التصدير إلى صفحة ثابتة بتنسيق HTML أو SVG.

عند تشغيل الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words . يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف. يُرجى ملاحظة أن أسماء الملفات يجب أن تكون فريدة.

يُنشئ Aspose.Words تلقائيًا اسم ملف فريد لكل مورد عند تصدير إلى تنسيق HTML أو SVG لصفحة ثابتة. تعتمد طريقة إنشاء اسم ملف المورد على ما إذا كنت تحفظ المستند في ملف أو في مسار.

عند حفظ مستند في ملف، يبدو اسم ملف الموارد الناتج مثل &lt;اسم ملف قاعدة المستند&gt;.&lt;رقم الصورة&gt;.&lt;الامتداد&gt;.

عند حفظ مستند في مجرى، يبدو اسم ملف الموارد الناتج مثل Aspose.Words.&lt;دليل المستند&gt;.&lt;رقم الصورة&gt;.&lt;الامتداد&gt;.

`ResourceFileName` يجب أن يحتوي فقط على اسم الملف بدون المسار. يحدد Aspose.Words المسار للحفظ وقيمة`المصدر` سمة لكتابة إلى صفحة HTML أو SVG ثابتة باستخدام اسم ملف المستند،[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) أو[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) و[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) أو[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) ملكيات.

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
