---
title: PageLayoutCallbackArgs.Event
second_title: Aspose.Words لمراجع .NET API
description: PageLayoutCallbackArgs ملكية. يحصل على الحدث.
type: docs
weight: 20
url: /ar/net/aspose.words.layout/pagelayoutcallbackargs/event/
---
## PageLayoutCallbackArgs.Event property

يحصل على الحدث.

```csharp
public PageLayoutEvent Event { get; }
```

### أمثلة

يوضح كيفية تتبع تغييرات التخطيط مع استدعاء التخطيط.

```csharp
[Test]
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
/// ويعرض صفحة ننفذها لإعادة تدفق الصفحة إلى صورة في نظام الملفات المحلي.
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

* enum [PageLayoutEvent](../../pagelayoutevent/)
* class [PageLayoutCallbackArgs](../)
* مساحة الاسم [Aspose.Words.Layout](../../pagelayoutcallbackargs/)
* المجسم [Aspose.Words](../../../)


