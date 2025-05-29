---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup DifferentFirstPageHeaderFooter لتخصيص الصفحة الأولى من مستندك باستخدام رؤوس وتذييلات فريدة لإضفاء لمسة احترافية.
type: docs
weight: 110
url: /ar/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

صحيح إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

يوضح كيفية تمكين أو تعطيل الرؤوس/التذييلات الأساسية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان من الرؤوس والتذييلات.
// 1 - "الرأس/التذييل الأول"، والذي يظهر في الصفحة الأولى من القسم.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - الرأس/التذييل "الأساسي"، والذي يظهر في كل صفحة في القسم.
// يمكننا تجاوز الرأس/التذييل الأساسي برأس/تذييل الصفحة الأولى ورأس/تذييل الصفحة الزوجية.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// يحتوي كل قسم على كائن "PageSetup" الذي يحدد خصائص مرتبطة بمظهر الصفحة
// مثل الاتجاه والحجم والحدود.
// قم بضبط الخاصية "DifferentFirstPageHeaderFooter" على "true" لتطبيق أول رأس/تذييل على الصفحة الأولى.
// اضبط خاصية "DifferentFirstPageHeaderFooter" على "false"
// لجعل الصفحة الأولى تعرض الرأس/التذييل الأساسي.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

يوضح كيفية تتبع الترتيب الذي تمر به عملية استبدال النص عبر العقد.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // استخدام رأس/تذييل مختلف للصفحة الأولى سيؤثر على ترتيب البحث.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// أثناء عملية البحث والاستبدال، يتم تسجيل محتويات كل عقدة تحتوي على نص "تجده" العملية،
/// في الحالة التي كانت عليها قبل أن يتم الاستبدال.
/// سيؤدي هذا إلى عرض الترتيب الذي تمر به عملية استبدال النص عبر العقد.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
