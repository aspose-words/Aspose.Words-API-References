---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.IPageLayoutCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي يتم استدعاؤها أثناء إنشاء نموذج تخطيط الصفحة وعرضه في C#.
type: docs
weight: 3310
url: /ar/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي يتم استدعاؤها أثناء إنشاء نموذج تخطيط الصفحة وعرضه.

```csharp
public interface IPageLayoutCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | يتم استدعاؤه للإخطار ببناء التخطيط وتقديم التقدم. |

## ملاحظات

الاستخدام الأساسي لهذه الواجهة هو السماح لكود التطبيق بإحباط عملية الإنشاء.

من الممكن إنشاء نموذج تخطيط صفحة لعدد قليل من الصفحات فقط في بداية المستند ثم إحباط العملية وعرض ما تم إنشاؤه بالفعل فقط.

مع ذلك، لاحظ أن نتائج العرض قد لا تتطابق مع ما سيتم عرضه لكل صفحة إذا كانت العملية قد انتهت.

قد لا تعمل هذه التقنية مع كل مستند أو قد تفشل تمامًا.

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

* property [Callback](../layoutoptions/callback/)
* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
