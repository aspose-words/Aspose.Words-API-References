---
title: IPageLayoutCallback.Notify
second_title: Aspose.Words لمراجع .NET API
description: IPageLayoutCallback طريقة. يتم استدعاؤه للإخطار ببناء التخطيط وتقديم التقدم.
type: docs
weight: 10
url: /ar/net/aspose.words.layout/ipagelayoutcallback/notify/
---
## IPageLayoutCallback.Notify method

يتم استدعاؤه للإخطار ببناء التخطيط وتقديم التقدم.

```csharp
public void Notify(PageLayoutCallbackArgs args)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| args | PageLayoutCallbackArgs | حجة الحدث. |

### ملاحظات

الاستثناء عند طرحه بواسطة التنفيذ يجهض عملية بناء التخطيط.

### أمثلة

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

* class [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/)
* interface [IPageLayoutCallback](../)
* مساحة الاسم [Aspose.Words.Layout](../../ipagelayoutcallback/)
* المجسم [Aspose.Words](../../../)


