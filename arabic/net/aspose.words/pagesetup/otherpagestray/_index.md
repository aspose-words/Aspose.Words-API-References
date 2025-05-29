---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup OtherPagesTray لتخصيص إعدادات درج الورق لطابعتك بسهولة. حسّن كفاءة الطباعة في كل قسم!
type: docs
weight: 300
url: /ar/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

يحصل على درج الورق (الحاوية) الذي سيتم استخدامه لجميع الصفحات باستثناء الصفحة الأولى من القسم أو يعينه. القيمة خاصة بالتنفيذ (الطابعة).

```csharp
public int OtherPagesTray { get; set; }
```

## أمثلة

يوضح كيفية جعل كافة الأقسام في مستند تستخدم درج الورق الافتراضي للطابعة المحددة.

```csharp
Document doc = new Document();

// ابحث عن الطابعة الافتراضية التي سنستخدمها لطباعة هذا المستند.
// يمكنك تعريف طابعة معينة باستخدام خاصية "PrinterName" في كائن PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// قيمة درج الورق المخزنة في المستندات خاصة بالطابعة.
// هذا يعني أن الكود أدناه يعيد تعيين جميع قيم درج الصفحات لاستخدام درج الطابعة الافتراضي الحالي.
// يمكنك تعداد PrinterSettings.PaperSources للعثور على قيم درج الورق الصالحة الأخرى للطابعة المحددة.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

يوضح كيفية إعداد الطباعة باستخدام أدراج الطابعة المختلفة لأحجام الورق المختلفة.

```csharp
Document doc = new Document();

// ابحث عن الطابعة الافتراضية التي سنستخدمها لطباعة هذا المستند.
// يمكنك تعريف طابعة معينة باستخدام خاصية "PrinterName" في كائن PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// هذه هي الدرج الذي سنستخدمه للصفحات بحجم ورق "A4".
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// هذه هي الدرج الذي سنستخدمه للصفحات بحجم ورق "Letter".
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// تعديل كائن PageSettings في هذا القسم لجعل Microsoft Word يصدر تعليمات للطابعة
// لاستخدام أحد الصواني التي حددناها أعلاه، اعتمادًا على حجم الورق في هذا القسم.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
