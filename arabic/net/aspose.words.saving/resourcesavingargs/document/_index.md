---
title: ResourceSavingArgs.Document
second_title: Aspose.Words لمراجع .NET API
description: ResourceSavingArgs ملكية. الحصول على كائن المستند الذي يتم حفظه حاليًا.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

الحصول على كائن المستند الذي يتم حفظه حاليًا.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../resourcesavingargs/)
* المجسم [Aspose.Words](../../../)


