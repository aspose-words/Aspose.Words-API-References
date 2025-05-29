---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words لـ .NET
description: خصّص تخطيط مستندك باستخدام واجهة Aspose.Words.Layout.IPageLayoutCallback. حسّن العرض بطرقك الخاصة لتحقيق أفضل النتائج.
type: docs
weight: 3760
url: /ar/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء بناء وعرض نموذج تخطيط الصفحة.

```csharp
public interface IPageLayoutCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | يتم استدعاء هذا لإعلامك ببناء التخطيط وتقدم العرض. |

## ملاحظات

الاستخدام الأساسي لهذه الواجهة هو السماح لكود التطبيق بإلغاء عملية البناء.

من الممكن إنشاء نموذج تخطيط الصفحة لعدد قليل من الصفحات في بداية المستند ثم إلغاء العملية وعرض ما تم بناؤه بالفعل فقط.

ومع ذلك، لاحظ أن نتائج العرض قد لا تتطابق مع ما سيتم عرضه لكل صفحة إذا انتهت العملية.

قد لا تنجح هذه التقنية مع كل المستندات أو قد تفشل تمامًا.

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

* property [Callback](../layoutoptions/callback/)
* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
