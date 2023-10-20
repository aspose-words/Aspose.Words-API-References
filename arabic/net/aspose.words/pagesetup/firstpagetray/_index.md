---
title: PageSetup.FirstPageTray
linktitle: FirstPageTray
articleTitle: FirstPageTray
second_title: Aspose.Words لـ .NET
description: PageSetup FirstPageTray ملكية. الحصول على أو تعيين درج الورق الحاوية لاستخدامه في الصفحة الأولى من القسم. القيمة خاصة بالتنفيذ الطابعة في C#.
type: docs
weight: 130
url: /ar/net/aspose.words/pagesetup/firstpagetray/
---
## PageSetup.FirstPageTray property

الحصول على أو تعيين درج الورق (الحاوية) لاستخدامه في الصفحة الأولى من القسم. القيمة خاصة بالتنفيذ (الطابعة).

```csharp
public int FirstPageTray { get; set; }
```

## أمثلة

يوضح كيفية جعل كافة الأقسام الموجودة في المستند تستخدم درج الورق الافتراضي للطابعة المحددة.

```csharp
Document doc = new Document();

// ابحث عن الطابعة الافتراضية التي سنستخدمها لطباعة هذا المستند.
// يمكنك تحديد طابعة معينة باستخدام خاصية "PrinterName" لكائن PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// قيمة درج الورق المخزنة في المستندات خاصة بالطابعة.
// هذا يعني أن الكود الموجود أدناه يعيد تعيين كافة قيم علبة الصفحات لاستخدام الدرج الافتراضي للطابعة الحالية.
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
// يمكنك تحديد طابعة معينة باستخدام خاصية "PrinterName" لكائن PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// هذا هو الدرج الذي سنستخدمه للصفحات بحجم ورق "A4".
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// هذا هو الدرج الذي سنستخدمه للصفحات بحجم ورق "Letter".
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// قم بتعديل كائن PageSettings في هذا القسم للحصول على Microsoft Word لتوجيه الطابعة
// لاستخدام أحد الأدراج التي حددناها أعلاه، اعتمادًا على حجم ورق هذا القسم.
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
