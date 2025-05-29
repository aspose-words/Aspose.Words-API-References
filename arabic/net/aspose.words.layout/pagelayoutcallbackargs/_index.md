---
title: PageLayoutCallbackArgs Class
linktitle: PageLayoutCallbackArgs
articleTitle: PageLayoutCallbackArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Layout.PageLayoutCallbackArgs لإدارة تخطيط المستندات بكفاءة. حسّن سير عملك بميزات إشعارات فعّالة.
type: docs
weight: 3810
url: /ar/net/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class

تم تمرير وسيطة إلى[`Notify`](../ipagelayoutcallback/notify/)

لمعرفة المزيد، قم بزيارة[التحويل إلى تنسيق الصفحة الثابتة](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) مقالة توثيقية.

```csharp
public class PageLayoutCallbackArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.layout/pagelayoutcallbackargs/document/) { get; } | يحصل على المستند. |
| [Event](../../aspose.words.layout/pagelayoutcallbackargs/event/) { get; } | يحصل على الحدث. |
| [PageIndex](../../aspose.words.layout/pagelayoutcallbackargs/pageindex/) { get; } | يحصل على فهرس قائم على 0 للصفحة في المستند الذي يرتبط به هذا الحدث. يعيد قيمة سلبية إذا لم تكن هناك صفحة مرتبطة، أو إذا تمت إزالة الصفحة أثناء إعادة التدفق. |

## أمثلة

يوضح كيفية تتبع تغييرات التخطيط باستخدام استدعاء التخطيط.

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// يخطرنا عندما نحفظ المستند بتنسيق صفحة ثابت
/// ويقوم بعرض صفحة نقوم بإعادة ترتيب صفحاتها على صورة في نظام الملفات المحلي.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
