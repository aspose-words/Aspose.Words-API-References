---
title: ResourceSavingArgs.ResourceFileName
second_title: Aspose.Words لمراجع .NET API
description: ResourceSavingArgs ملكية. الحصول على أو تحديد اسم الملف بدون مسار حيث سيتم حفظ المورد فيه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ المورد فيه.

```csharp
public string ResourceFileName { get; set; }
```

### ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات المصدر أثناء التصدير إلى صفحة ثابتة بتنسيق HTML أو SVG.

عند إطلاق الحدث ، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words . يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف . لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل مورد عند تصدير إلى تنسيق HTML أو SVG للصفحة الثابتة. تعتمد كيفية إنشاء اسم ملف المورد على ما إذا كنت ستحفظ المستند إلى ملف أو إلى دفق.

عند حفظ مستند إلى ملف ، يبدو اسم ملف المورد الناتج مثل &lt;اسم الملف الأساسي للمستند&gt;. &lt;رقم الصورة&gt;. &lt;امتداد&gt;.

عند حفظ مستند إلى دفق ، يبدو اسم ملف المورد الناتج مثل Aspose.Words. &lt;document GU&gt;. &lt;image number&gt;. &lt;extension&gt;.

`ResourceFileName` يجب أن يحتوي على اسم الملف فقط بدون المسار. Aspose. تحدد الكلمات مسار الحفظ وقيمة`src` السمة لكتابة لصفحة HTML أو SVG ثابتة باستخدام اسم ملف المستند ، و[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) أو[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) و[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) أو[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) الخصائص.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../resourcesavingargs/)
* المجسم [Aspose.Words](../../../)


