---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Layout.PageLayoutEvent، وهي ضرورية لتحسين أحداث تخطيط الصفحات أثناء عرض المستندات وإنشائها. حسّن سير عملك اليوم!
type: docs
weight: 3820
url: /ar/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

رمز الحدث الذي تم إثارته أثناء بناء نموذج تخطيط الصفحة وتقديمه.

يتم بناء نموذج تخطيط الصفحة في خطوتين. أولاً، "خطوة التحويل"، وهذا عندما يسحب تخطيط الصفحة محتوى المستند وينشئ رسمًا بيانيًا للكائنات. ثانيًا، "خطوة إعادة التدفق"، وهذا عندما يتم تقسيم الهياكل ودمجها وترتيبها في الصفحات.

اعتمادًا على العملية التي أدت إلى إنشاء النموذج، قد يتم أو لا يتم تقديم نموذج تخطيط الصفحة إلى تنسيق صفحة ثابت. على سبيل المثال، لا يتطلب حساب عدد الصفحات في المستند أو تحديث الحقول تقديمًا، بينما يتطلب التصدير إلى ملف Pdf تقديمًا.

```csharp
public enum PageLayoutEvent
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | القيمة الافتراضية |
| WatchDog | `1` | يتوافق مع نقطة تفتيش في الكود يتم زيارتها بشكل متكرر والتي تكون مناسبة لإلغاء العملية. |
| BuildStarted | `2` | بدأ بناء تخطيط الصفحة. تم تشغيله مرة واحدة. هذا هو الحدث الأول الذي يحدث عند[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يُسمى. |
| BuildFinished | `3` | انتهى بناء تخطيط الصفحة. تم تشغيله مرة واحدة. هذا هو آخر حدث يحدث عند[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) يُسمى. |
| ConversionStarted | `4` | بدأ تحويل نموذج المستند إلى تخطيط الصفحة. تم تشغيله مرة واحدة. يحدث هذا عندما يبدأ نموذج التخطيط بسحب محتوى المستند. |
| ConversionFinished | `5` | انتهى تحويل نموذج المستند إلى تخطيط الصفحة. تم تشغيله مرة واحدة. يحدث هذا عندما يتوقف نموذج التخطيط عن سحب محتوى المستند. |
| ReflowStarted | `6` | بدأت إعادة تدفق تخطيط الصفحة. تم تشغيلها مرة واحدة. يحدث هذا عندما يبدأ نموذج التخطيط بإعادة تدفق محتوى المستند. |
| ReflowFinished | `7` | انتهت عملية إعادة تدفق تخطيط الصفحة. تم تنفيذها مرة واحدة. يحدث هذا عندما يتوقف نموذج التخطيط عن إعادة تدفق محتوى المستند. |
| PartReflowStarted | `8` | بدأت عملية إعادة تدفق الصفحة. لاحظ أن الصفحة قد تتم إعادة تدفقها عدة مرات وقد تتم إعادة تشغيل عملية إعادة التدفق قبل الانتهاء منها. |
| PartReflowFinished | `9` | انتهت عملية إعادة تدفق الصفحة. لاحظ أن الصفحة قد تتم إعادة تدفقها عدة مرات وقد تتم إعادة تشغيل عملية إعادة التدفق قبل الانتهاء منها. |
| PartRenderingStarted | `10` | بدأ عرض الصفحة. يُفعّل هذا مرة واحدة لكل صفحة. |
| PartRenderingFinished | `11` | انتهى عرض الصفحة. يتم تشغيل هذا مرة واحدة لكل صفحة. |

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
