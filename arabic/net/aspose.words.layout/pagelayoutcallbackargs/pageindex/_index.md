---
title: PageLayoutCallbackArgs.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words لـ .NET
description: PageLayoutCallbackArgs PageIndex ملكية. الحصول على فهرس يستند إلى 0 للصفحة في المستند الذي يتعلق به هذا الحدث. إرجاع قيمة سالبة إذا لم تكن هناك صفحة مرتبطة أو إذا تمت إزالة الصفحة أثناء إعادة التدفق في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.layout/pagelayoutcallbackargs/pageindex/
---
## PageLayoutCallbackArgs.PageIndex property

الحصول على فهرس يستند إلى 0 للصفحة في المستند الذي يتعلق به هذا الحدث. إرجاع قيمة سالبة إذا لم تكن هناك صفحة مرتبطة، أو إذا تمت إزالة الصفحة أثناء إعادة التدفق.

```csharp
public int PageIndex { get; }
```

## أمثلة

يوضح كيفية تتبع تغييرات التخطيط من خلال رد اتصال التخطيط.

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
/// ويعرض الصفحة التي نقوم بإعادة تدفق الصفحة عليها إلى صورة في نظام الملفات المحلي.
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

* class [PageLayoutCallbackArgs](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
