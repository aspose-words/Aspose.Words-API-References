---
title: ExportListLabels Enum
linktitle: ExportListLabels
articleTitle: ExportListLabels
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ExportListLabels تعداد. يحدد كيفية تصدير تسميات القائمة إلى HTML وMHTML وEPUB في C#.
type: docs
weight: 5010
url: /ar/net/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enumeration

يحدد كيفية تصدير تسميات القائمة إلى HTML وMHTML وEPUB.

```csharp
public enum ExportListLabels
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | تسميات قائمة المخرجات في الوضع التلقائي. يستخدم عناصر HTML الأصلية عندما يكون ذلك ممكنًا. |
| AsInlineText | `1` | إخراج كافة تسميات القائمة كنص مضمن. |
| ByHtmlTags | `2` | إخراج كافة تسميات القائمة كعناصر HTML أصلية. |

## أمثلة

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

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد عناصر HTML التي سيستخدمها المستند لتمثيل القوائم.
// ضبط خاصية "ExportListLabels" على "ExportListLabels.AsInlineText"
// سيُنشئ قوائم بتنسيق الامتدادات.
// سيؤدي تعيين خاصية "ExportListLabels" إلى "ExportListLabels.Auto" إلى استخدام <p> بطاقة شعار
// لإنشاء قوائم في الحالات عند استخدام <ol> <لي> قد تتسبب العلامات في فقدان التنسيق.
// ضبط خاصية "ExportListLabels" على "ExportListLabels.ByHtmlTags"
// سوف يستخدم <ol> <لي> العلامات لبناء كافة القوائم.
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
        break;
    case ExportListLabels.ByHtmlTags:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));
        break;
}
```

### أنظر أيضا

* property [ExportListLabels](../htmlsaveoptions/exportlistlabels/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
