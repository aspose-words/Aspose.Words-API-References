---
title: Enum ResourceLoadingAction
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Loading.ResourceLoadingAction تعداد. يحدد طريقة تحميل الموارد.
type: docs
weight: 3680
url: /ar/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

يحدد طريقة تحميل الموارد.

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public enum ResourceLoadingAction
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | سيقوم Aspose.Words بتحميل هذا المورد كالمعتاد. |
| Skip | `1` | سوف يتخطى Aspose.Words تحميل هذا المورد. سيتم تخزين الرابط الذي لا يحتوي على بيانات فقط للصورة، وسيتم تجاهل ورقة أنماط CSS لتنسيق HTML. |
| UserProvided | `2` | سوف يستخدم Aspose.Words مصفوفة البايت التي يوفرها المستخدم[`SetData`](../resourceloadingargs/setdata/) كبيانات الموارد. |

### أمثلة

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // عادة ما يتم إدراج الصور باستخدام URI، أو مصفوفة بايت.
    // كل مثيل لتحميل المورد سوف يستدعي طريقة ResourceLoading الخاصة برد الاتصال الخاص بنا.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// يسمح لنا بتحميل الصور في مستند باستخدام اختصارات محددة مسبقًا، بدلاً من عناوين URI.
/// سيؤدي هذا إلى فصل منطق تحميل الصورة عن بقية إنشاء المستند.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // إذا واجه رد الاتصال هذا أحد اختصارات الصورة أثناء تحميل الصورة،
        // سيتم تطبيق منطق فريد لكل اختصار محدد بدلاً من معاملته كعنوان URI.
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


