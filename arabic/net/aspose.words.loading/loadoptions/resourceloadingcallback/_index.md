---
title: LoadOptions.ResourceLoadingCallback
linktitle: ResourceLoadingCallback
articleTitle: ResourceLoadingCallback
second_title: Aspose.Words لـ .NET
description: حسّن استيراد مستنداتك باستخدام ResourceLoadingCallback من LoadOptions. تحكّم بسلاسة في تحميل الموارد الخارجية، مثل الصور وأوراق الأنماط.
type: docs
weight: 140
url: /ar/net/aspose.words.loading/loadoptions/resourceloadingcallback/
---
## LoadOptions.ResourceLoadingCallback property

يسمح بالتحكم في كيفية تحميل الموارد الخارجية (الصور، أوراق الأنماط) عند استيراد مستند من HTML، MHTML.

```csharp
public IResourceLoadingCallback ResourceLoadingCallback { get; set; }
```

## أمثلة

يوضح كيفية التعامل مع الموارد الخارجية عند تحميل مستندات HTML.

```csharp
public void LoadOptionsCallback()
{
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.ResourceLoadingCallback = new HtmlLinkedResourceLoadingCallback();

    // عندما نقوم بتحميل المستند، ستتعامل وظيفة معاودة الاتصال لدينا مع الموارد المرتبطة مثل أوراق أنماط CSS والصور.
    Document doc = new Document(MyDir + "Images.html", loadOptions);
    doc.Save(ArtifactsDir + "LoadOptions.LoadOptionsCallback.pdf");
}

/// <summary>
/// يطبع أسماء الملفات لجميع أوراق الأنماط الخارجية ويستبدل جميع الصور الموجودة في مستند HTML المحمل.
/// </summary>
private class HtmlLinkedResourceLoadingCallback : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        switch (args.ResourceType)
        {
            case ResourceType.CssStyleSheet:
                Console.WriteLine($"External CSS Stylesheet found upon loading: {args.OriginalUri}");
                return ResourceLoadingAction.Default;
            case ResourceType.Image:
                Console.WriteLine($"External Image found upon loading: {args.OriginalUri}");

                const string newImageFilename = "Logo.jpg";
                Console.WriteLine($"\tImage will be substituted with: {newImageFilename}");

                Image newImage = Image.FromFile(ImageDir + newImageFilename);

                ImageConverter converter = new ImageConverter();
                byte[] imageBytes = (byte[])converter.ConvertTo(newImage, typeof(byte[]));
                args.SetData(imageBytes);

                return ResourceLoadingAction.UserProvided;
        }

        return ResourceLoadingAction.Default;
    }
}
```

### أنظر أيضا

* interface [IResourceLoadingCallback](../../iresourceloadingcallback/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
