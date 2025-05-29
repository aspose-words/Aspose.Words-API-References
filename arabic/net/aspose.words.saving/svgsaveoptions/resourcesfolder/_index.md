---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية ضبط مجلد الموارد في خيارات حفظ Svg لتخزين الصور بكفاءة عند تصدير المستندات بتنسيق SVG. حسّن سير عملك اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

يحدد المجلد الفعلي الذي يتم حفظ الموارد (الصور) فيه عند تصدير مستند إلى تنسيق Svg. الافتراضي هو`باطل` .

```csharp
public string ResourcesFolder { get; set; }
```

## ملاحظات

لا يكون له تأثير إلا إذا[`ExportEmbeddedImages`](../exportembeddedimages/) الممتلكات هي`خطأ شنيع`.

عندما تحفظ[`Document`](../../../aspose.words/document/) في تنسيق SVG، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة.`ResourcesFolder` يسمح لك بتحديد المكان الذي سيتم حفظ الصور فيه و[`ResourcesFolderAlias`](../resourcesfolderalias/) يسمح لك بتحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وأدخلت اسمًا للملف، فسيحفظ Aspose.Words افتراضيًا صور x000d_ في نفس المجلد الذي حُفظ فيه ملف المستند. استخدم`ResourcesFolder` لتجاوز هذا السلوك.

إذا حفظت مستندًا في مسار، فلن يحتوي Aspose.Words على مجلد لحفظ الصور، ، ولكنه سيحتاج إلى حفظ الصور في مكان ما. في هذه الحالة، ستحتاج إلى تحديد مجلد يسهل الوصول إليه في`ResourcesFolder` ملكية

## أمثلة

يوضح كيفية التعامل مع عناوين URI للموارد المرتبطة وطباعتها والتي تم إنشاؤها أثناء تحويل مستند إلى .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// يقوم بحساب وطباعة عناوين URI للموارد المضمنة بواسطة أثناء تحويلها إلى .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
