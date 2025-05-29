---
title: IPageLayoutCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة iPageLayoutCallback Notify لتحسين كفاءة بناء المخططات وعرضها. حسّن أداء تطبيقك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.layout/ipagelayoutcallback/notify/
---
## IPageLayoutCallback.Notify method

يتم استدعاء هذا لإعلامك ببناء التخطيط وتقدم العرض.

```csharp
public void Notify(PageLayoutCallbackArgs args)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| args | PageLayoutCallbackArgs | حجة الحدث. |

## ملاحظات

استثناء عند إلقائه بواسطة التنفيذ يلغى عملية بناء التخطيط.

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

* class [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/)
* interface [IPageLayoutCallback](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
