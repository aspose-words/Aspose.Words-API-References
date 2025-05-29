---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Loading.ResourceLoadingArgs، المصممة لتحسين كفاءة تحميل الموارد في تطبيقاتك. تكامل سلس اليوم!
type: docs
weight: 4150
url: /ar/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

يوفر بيانات لـ[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) الطريقة.

```csharp
public class ResourceLoadingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | عنوان URI الأصلي للمورد كما هو محدد في المستند المستورد. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | نوع المورد. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI للمورد المستخدم لتنزيل إذا[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) يعودDefault. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | يحدد البيانات المقدمة من المستخدم للمورد الذي يتم استخدامه إذا[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) يعودUserProvided . |

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
