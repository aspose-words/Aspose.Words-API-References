---
title: Enum PageLayoutEvent
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Layout.PageLayoutEvent تعداد. رمز الحدث الذي تم رفعه أثناء إنشاء نموذج تخطيط الصفحة وعرضه.
type: docs
weight: 3370
url: /ar/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

رمز الحدث الذي تم رفعه أثناء إنشاء نموذج تخطيط الصفحة وعرضه.

يتم إنشاء نموذج تخطيط الصفحة في خطوتين. أولاً، "خطوة التحويل"، وذلك عندما يقوم تخطيط الصفحة بسحب محتوى المستند وإنشاء رسم بياني للكائن. ثانيًا، "خطوة إعادة التدفق"، وذلك عندما يتم تقسيم الهياكل ودمجها وترتيبها في الصفحات.

اعتمادًا على العملية التي أدت إلى الإنشاء، قد يتم أو لا يتم عرض نموذج تخطيط الصفحة إلى تنسيق صفحة ثابت. على سبيل المثال، لا يتطلب حساب عدد الصفحات في المستند أو تحديث الحقول العرض، في حين أن التصدير إلى Pdf يتطلب ذلك.

```csharp
public enum PageLayoutEvent
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية |
| WatchDog | `1` | يتوافق مع نقطة التحقق في الكود التي تتم زيارتها غالبًا والتي تكون مناسبة لإلغاء العملية. |
| BuildStarted | `2` | بدأ إنشاء تخطيط الصفحة. تم إطلاقه مرة واحدة. هذا هو الحدث الأول الذي يحدث عندما[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يسمى. |
| BuildFinished | `3` | تم الانتهاء من بناء تخطيط الصفحة. تم إطلاقه مرة واحدة. هذا هو الحدث الأخير الذي يحدث عندما[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يسمى. |
| ConversionStarted | `4` | بدأ تحويل نموذج المستند إلى تخطيط الصفحة. تم التشغيل مرة واحدة. يحدث هذا عندما يبدأ نموذج التخطيط في سحب محتوى المستند. |
| ConversionFinished | `5` | تم الانتهاء من تحويل نموذج المستند إلى تخطيط الصفحة. تم التشغيل مرة واحدة. ويحدث هذا عندما يتوقف نموذج التخطيط عن سحب محتوى المستند. |
| ReflowStarted | `6` | بدأ إعادة تدفق تخطيط الصفحة. تم التشغيل مرة واحدة. يحدث هذا عندما يبدأ نموذج التخطيط في إعادة تدفق محتوى المستند. |
| ReflowFinished | `7` | تم الانتهاء من إعادة تدفق تخطيط الصفحة. تم التشغيل مرة واحدة. يحدث هذا عندما يتوقف نموذج التخطيط عن إعادة تدفق محتوى المستند. |
| PartReflowStarted | `8` | بدأ إعادة التدفق للصفحة. لاحظ أن الصفحة قد تتم إعادة التدفق عدة مرات وقد يتم إعادة تشغيل إعادة التدفق قبل الانتهاء. |
| PartReflowFinished | `9` | انتهت عملية إعادة التدفق للصفحة. لاحظ أن الصفحة قد تتم إعادة التدفق عدة مرات وقد يتم إعادة تشغيل عملية إعادة التدفق هذه قبل الانتهاء. |
| PartRenderingStarted | `10` | بدأ عرض الصفحة. يتم إطلاق هذا مرة واحدة لكل صفحة. |
| PartRenderingFinished | `11` | انتهى عرض الصفحة. يتم إطلاق هذا مرة واحدة لكل صفحة. |

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)


