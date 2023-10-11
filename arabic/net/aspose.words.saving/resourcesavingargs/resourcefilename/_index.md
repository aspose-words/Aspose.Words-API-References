---
title: ResourceSavingArgs.ResourceFileName
second_title: Aspose.Words لمراجع .NET API
description: ResourceSavingArgs ملكية. الحصول على أو تعيين اسم الملف بدون مسار حيث سيتم حفظ المورد فيه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

الحصول على أو تعيين اسم الملف (بدون مسار) حيث سيتم حفظ المورد فيه.

```csharp
public string ResourceFileName { get; set; }
```

### ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات الموارد أثناء التصدير إلى صفحة ثابتة بتنسيق HTML أو SVG.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل مورد عند تصدير إلى تنسيق HTML أو SVG لصفحة ثابتة. تعتمد كيفية إنشاء اسم ملف المورد على ما إذا كنت تقوم بحفظ المستند في ملف أو في دفق.

عند حفظ مستند في ملف، يبدو اسم ملف المورد الذي تم إنشاؤه مثل &lt;اسم الملف الأساسي للمستند&gt;.&lt;رقم الصورة&gt;.&lt;الامتداد&gt;.

عند حفظ مستند في دفق، يبدو اسم ملف المورد الذي تم إنشاؤه مثل Aspose.Words.&lt;document guid&gt;.&lt;image number&gt;.&lt;extension&gt;.

`ResourceFileName` يجب أن يحتوي فقط على اسم الملف بدون المسار. يحدد Aspose.Words مسار الحفظ وقيمة الملف`src` سمة لكتابة إلى صفحة ثابتة بتنسيق HTML أو SVG باستخدام اسم ملف المستند،[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) أو[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) و[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) أو[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) ملكيات.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

### أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../resourcesavingargs/)
* المجسم [Aspose.Words](../../../)


