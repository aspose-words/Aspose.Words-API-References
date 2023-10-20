---
title: FieldToc.CustomStyles
linktitle: CustomStyles
articleTitle: CustomStyles
second_title: Aspose.Words لـ .NET
description: FieldToc CustomStyles ملكية. الحصول على أو تعيين قائمة من الأنماط بخلاف أنماط العناوين المضمنة لتضمينها في جدول المحتويات في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldtoc/customstyles/
---
## FieldToc.CustomStyles property

الحصول على أو تعيين قائمة من الأنماط بخلاف أنماط العناوين المضمنة لتضمينها في جدول المحتويات.

```csharp
public string CustomStyles { get; set; }
```

## أمثلة

يوضح كيفية إدراج جدول محتويات، وتعبئته بالإدخالات بناءً على أنماط العناوين.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // أدخل حقل جدول المحتويات، الذي سيجمع كل العناوين في جدول المحتويات.
    // لكل عنوان، سينشئ هذا الحقل سطرًا يحتوي على النص بنمط العنوان هذا على اليسار،
    // والصفحة التي يظهر فيها العنوان على اليمين.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // استخدم خاصية BookmarkName لسرد العناوين فقط
    // التي تظهر ضمن حدود الإشارة المرجعية باسم "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // سيتم احتساب النص الذي يحتوي على نمط عنوان مدمج، مثل "العنوان 1"، المطبق عليه كعنوان.
    // يمكننا تسمية الأنماط الإضافية التي سيتم التقاطها كعناوين بواسطة جدول المحتويات في هذه الخاصية ومستويات جدول المحتويات الخاصة بها.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // افتراضيًا، يتم فصل مستويات الأنماط/جدول المحتويات في خاصية CustomStyles بفاصلة،
    // ولكن يمكننا تعيين محدد مخصص في هذه الخاصية.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // قم بتكوين الحقل لاستبعاد أي عناوين تحتوي على مستويات جدول المحتويات خارج هذا النطاق.
    field.HeadingLevelRange = "1-3";

    // لن يعرض جدول المحتويات أرقام صفحات العناوين التي تقع مستويات جدول المحتويات الخاصة بها ضمن هذا النطاق.
    field.PageNumberOmittingLevelRange = "2-5";

     // قم بتعيين سلسلة مخصصة تفصل كل عنوان عن رقم الصفحة الخاص به.
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

    // سيتم حذف أرقام الصفحات في هذين العنوانين لأنها تقع ضمن النطاق "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // لا يظهر هذا الإدخال لأن "العنوان 4" يقع خارج النطاق "1-3" الذي قمنا بتعيينه مسبقًا.
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
/// ابدأ صفحة جديدة وأدخل فقرة بنمط محدد.
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
