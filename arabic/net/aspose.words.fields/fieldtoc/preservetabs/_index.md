---
title: FieldToc.PreserveTabs
second_title: Aspose.Words لمراجع .NET API
description: FieldToc ملكية. يحصل أو يحدد ما إذا كان سيتم الاحتفاظ بإدخالات علامة التبويب داخل إدخالات الجدول.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldtoc/preservetabs/
---
## FieldToc.PreserveTabs property

يحصل أو يحدد ما إذا كان سيتم الاحتفاظ بإدخالات علامة التبويب داخل إدخالات الجدول.

```csharp
public bool PreserveTabs { get; set; }
```

### أمثلة

يوضح كيفية إدراج جدول المحتويات ، وملئه بالإدخالات بناءً على أنماط العناوين.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // أدخل حقل جدول المحتويات ، والذي سيجمع كل العناوين في جدول المحتويات.
    // لكل عنوان ، سينشئ هذا الحقل سطرًا بالنص الموجود في نمط العنوان هذا إلى اليسار ،
    // والصفحة التي يظهر عليها العنوان إلى اليمين.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // استخدم خاصية BookmarkName لقائمة العناوين فقط
    // التي تظهر داخل حدود إشارة مرجعية باسم "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // سيتم احتساب النص الذي يحتوي على نمط عنوان مضمّن ، مثل "العنوان 1" ، المطبق عليه كعنوان.
    // يمكننا تسمية أنماط إضافية ليتم التقاطها كعناوين بواسطة جدول المحتويات في هذه الخاصية ومستويات جدول المحتويات.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // افتراضيًا ، يتم فصل مستويات الأنماط / جدول المحتويات في خاصية CustomStyles بفاصلة ،
    // ولكن يمكننا تعيين محدد مخصص في هذه الخاصية.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // تكوين الحقل لاستبعاد أي عناوين لها مستويات جدول المحتويات خارج هذا النطاق.
    field.HeadingLevelRange = "1-3";

    // لن يعرض جدول المحتويات أرقام صفحات العناوين التي تقع مستويات جدول المحتويات ضمن هذا النطاق.
    field.PageNumberOmittingLevelRange = "2-5";

     // قم بتعيين سلسلة مخصصة تفصل كل عنوان عن رقم صفحته.
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

    // سيتم حذف أرقام الصفحات لهذين العنوانين لأنهما يقعان ضمن النطاق "2-5".
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

/// <summary>
/// ابدأ صفحة جديدة وأدخل فقرة من النمط المحدد.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldtoc/)
* المجسم [Aspose.Words](../../../)


