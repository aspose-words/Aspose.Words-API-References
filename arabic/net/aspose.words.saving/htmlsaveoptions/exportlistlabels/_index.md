---
title: ExportListLabels
second_title: Aspose.Words لمراجع .NET API
description: يتحكم في كيفية إخراج تسميات القوائم إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAuto .
type: docs
weight: 200
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportlistlabels/
---
## HtmlSaveOptions.ExportListLabels property

يتحكم في كيفية إخراج تسميات القوائم إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيAuto .

```csharp
public ExportListLabels ExportListLabels { get; set; }
```

### أمثلة

يوضح كيفية تكوين قائمة التصدير إلى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Aspose.Words.Lists.List list = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = list;

builder.Writeln("Default numbered list item 1.");
builder.Writeln("Default numbered list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Default numbered list item 3.");
builder.ListFormat.RemoveNumbers();

list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
builder.ListFormat.List = list;

builder.Writeln("Outline legal heading list item 1.");
builder.Writeln("Outline legal heading list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 3.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 4.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 5.");
builder.ListFormat.RemoveNumbers();

// عند حفظ المستند إلى HTML ، يمكننا تمرير كائن SaveOptions
// لتحديد عناصر HTML التي سيستخدمها المستند لتمثيل القوائم.
// تعيين خاصية "ExportListLabels" إلى "ExportListLabels.AsInlineText"
// سيُنشئ قوائم عن طريق تنسيق الامتدادات.
// تعيين خاصية "ExportListLabels" على "ExportListLabels.Auto" سيستخدم العلامة < p > بطاقة شعار
// لبناء قوائم في الحالات عند استخدام العلامة < ol > و < li > قد تتسبب العلامات في فقد التنسيق.
// تعيين خاصية "ExportListLabels" إلى "ExportListLabels.ByHtmlTags"
// سيستخدم العلامة < ol > و < li > العلامات لبناء جميع القوائم.
HtmlSaveOptions options = new HtmlSaveOptions { ExportListLabels = exportListLabels };

doc.Save(ArtifactsDir + "HtmlSaveOptions.List.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.List.html");

switch (exportListLabels)
{
    case ExportListLabels.AsInlineText:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>a.</span>" +
                    "<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Default numbered list item 3.</span>" +
            "</p>"));

        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>2.1.1.1</span>" +
                    "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Outline legal heading list item 5.</span>" +
            "</p>"));
        break;
    case ExportListLabels.Auto:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));

        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; " +
            "-aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; " +
            "-aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>2.1.1.1</span>" +
                    "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Outline legal heading list item 5.</span>" +
            "</p>"));
        break;
    case ExportListLabels.ByHtmlTags:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));

        Assert.True(outDocContents.Contains(
            "<ol type=\"1\" class=\"awlist3\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:7.2pt; text-indent:-43.2pt; -aw-list-padding-sml:10.2pt\">" +
                    "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:ignore\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                    "<span>Outline legal heading list item 5.</span>" +
                "</li>" +
            "</ol>"));
        break;
}
```

### أنظر أيضا

* enum [ExportListLabels](../../exportlistlabels/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
