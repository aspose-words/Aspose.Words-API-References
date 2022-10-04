---
title: DifferentFirstPageHeaderFooter
second_title: Aspose.Words لمراجع .NET API
description: حقيقي إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى.
type: docs
weight: 110
url: /ar/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

**حقيقي** إذا تم استخدام رأس أو تذييل مختلف في الصفحة الأولى.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

### أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوس وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// أنشئ الرؤوس ، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
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

يوضح كيفية تمكين أو تعطيل الرؤوس / التذييلات الأساسية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يوجد أدناه نوعان من الرؤوس / التذييلات.
// 1 - رأس / تذييل "الأول" ، والذي يظهر في الصفحة الأولى من القسم.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - الرأس / التذييل "الأساسي" ، والذي يظهر في كل صفحة في القسم.
// يمكننا تجاوز الرأس / التذييل الأساسي برأس / تذييل الصفحة الأولى والزوجية.
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

// يحتوي كل قسم على كائن "PageSetup" يحدد الخصائص المتعلقة بمظهر الصفحة
// مثل الاتجاه والحجم والحدود.
// قم بتعيين خاصية "DifferentFirstPageHeaderFooter" على "true" لتطبيق أول رأس / تذييل على الصفحة الأولى.
// تعيين خاصية "DifferentFirstPageHeaderFooter" إلى "false"
// لجعل الصفحة الأولى تعرض الرأس / التذييل الأساسي.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

يوضح كيفية تعقب الترتيب الذي تتجاوز به عملية استبدال النص العقد.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // سيؤثر استخدام رأس / تذييل مختلف للصفحة الأولى على ترتيب البحث.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0_OR_GREATER || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// أثناء عملية البحث والاستبدال ، يسجل محتويات كل عقدة تحتوي على نص "تعثر عليه" العملية ،
        /// في الحالة التي كانت عليها قبل حدوث الاستبدال.
        /// سيعرض هذا الترتيب الذي تتجاوز به عملية استبدال النص العقد.
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
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
