---
title: FieldToc.PreserveLineBreaks
linktitle: PreserveLineBreaks
articleTitle: PreserveLineBreaks
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldToc PreserveLineBreaks على تحسين إدخالات الجدول من خلال الحفاظ على أحرف السطر الجديد لتحسين قابلية القراءة والتنسيق.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/fieldtoc/preservelinebreaks/
---
## FieldToc.PreserveLineBreaks property

يحصل على أو يحدد ما إذا كان سيتم الاحتفاظ بأحرف السطر الجديد داخل إدخالات الجدول.

```csharp
public bool PreserveLineBreaks { get; set; }
```

## أمثلة

يوضح كيفية إدراج جدول المحتويات، وملئه بالإدخالات استنادًا إلى أنماط العنوان.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // أدخل حقل جدول المحتويات، والذي سيقوم بتجميع كافة العناوين في جدول المحتويات.
    // لكل عنوان، سيقوم هذا الحقل بإنشاء سطر يحتوي على النص الموجود في نمط العنوان هذا على اليسار،
    // والصفحة التي يظهر فيها العنوان على اليمين.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // استخدم خاصية BookmarkName لإدراج العناوين فقط
    // التي تظهر ضمن حدود الإشارة المرجعية باسم "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // سيتم احتساب النص الذي يحتوي على نمط عنوان مدمج، مثل "العنوان 1"، كعنوان.
    // يمكننا تسمية الأنماط الإضافية التي سيتم التقاطها كعناوين بواسطة جدول المحتويات في هذه الخاصية ومستويات جدول المحتويات الخاصة بها.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // بشكل افتراضي، يتم فصل مستويات الأنماط/جدول المحتويات في خاصية CustomStyles بفاصلة،
    // ولكن يمكننا تعيين فاصل مخصص في هذه الخاصية.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // قم بتكوين الحقل لاستبعاد أي عناوين تحتوي على مستويات جدول المحتويات خارج هذا النطاق.
    field.HeadingLevelRange = "1-3";

    // لن يعرض جدول المحتويات أرقام الصفحات للعناوين التي تقع مستويات جدول المحتويات الخاصة بها ضمن هذا النطاق.
    field.PageNumberOmittingLevelRange = "2-5";

     // تعيين سلسلة مخصصة لفصل كل عنوان عن رقم الصفحة.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // سيتم حذف أرقام الصفحات لهذين العنوانين لأنهما ضمن النطاق "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // لا يظهر هذا الإدخال لأن "العنوان 4" خارج النطاق "1-3" الذي حددناه سابقًا.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // لا يظهر هذا الإدخال لأنه خارج الإشارة المرجعية المحددة بواسطة جدول المحتويات.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// ابدأ صفحة جديدة وأدرج فقرة ذات نمط محدد.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### أنظر أيضا

* class [FieldToc](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
