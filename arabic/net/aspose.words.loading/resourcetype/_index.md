---
title: ResourceType Enum
linktitle: ResourceType
articleTitle: ResourceType
second_title: Aspose.Words لـ .NET
description: استكشف تعدد Aspose.Words.ResourceType لإدارة الموارد بكفاءة. حسّن معالجة مستنداتك مع خيارات تحميل متعددة.
type: docs
weight: 4160
url: /ar/net/aspose.words.loading/resourcetype/
---
## ResourceType enumeration

نوع المورد المحمّل.

```csharp
public enum ResourceType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Image | `0` | صورة. |
| Font | `1` | الخط |
| CssStyleSheet | `2` | ورقة أنماط CSS. |
| Document | `3` | مستند. |

## أمثلة

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادةً ما يتم إدراج الصور باستخدام URI أو مجموعة بايتات.
    // كل مثيل لتحميل المورد سوف يستدعي طريقة ResourceLoading الخاصة بإرجاعنا.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// يسمح لنا بتحميل الصور إلى مستند باستخدام اختصارات محددة مسبقًا، بدلاً من عناوين URI.
/// سيؤدي هذا إلى فصل منطق تحميل الصورة عن بقية بناء المستند.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // إذا واجهت هذه الاستدعاءات أحد اختصارات الصورة أثناء تحميل صورة،
        // سيتم تطبيق منطق فريد لكل اختصار محدد بدلاً من التعامل معه باعتباره URI.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
