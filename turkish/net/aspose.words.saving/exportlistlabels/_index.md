---
title: ExportListLabels Enum
linktitle: ExportListLabels
articleTitle: ExportListLabels
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.ExportListLabels enum'unun özelleştirilebilir liste etiketi seçenekleriyle HTML, MHTML ve EPUB dışa aktarımlarınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 5760
url: /tr/net/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enumeration

Liste etiketlerinin HTML, MHTML ve EPUB'a nasıl aktarılacağını belirtir.

```csharp
public enum ExportListLabels
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Otomatik modda liste etiketlerini çıktı olarak verir. Mümkün olduğunda HTML yerel öğelerini kullanır. |
| AsInlineText | `1` | Tüm liste etiketlerini satır içi metin olarak çıktı olarak verir. |
| ByHtmlTags | `2` | Tüm liste etiketlerini HTML yerel öğeleri olarak çıktı olarak verir. |

## Örnekler

Listelerin HTML'e aktarılmasının nasıl yapılandırılacağını gösterir.

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

// Belgeyi HTML'e kaydederken SaveOptions nesnesini geçirebiliriz
// Belgenin listeleri temsil etmek için hangi HTML öğelerini kullanacağına karar vermek için.
// "ExportListLabels" özelliğini "ExportListLabels.AsInlineText" olarak ayarlama
// span'ları biçimlendirerek listeler oluşturacaktır.
// "ExportListLabels" özelliğini "ExportListLabels.Auto" olarak ayarlamak <p> etiketini kullanacaktır
// <ol> ve <li> etiketlerinin kullanılmasının biçimlendirme kaybına yol açabileceği durumlarda listeler oluşturmak için.
// "ExportListLabels" özelliğini "ExportListLabels.ByHtmlTags" olarak ayarlama
// Tüm listeleri oluşturmak için <ol> ve <li> etiketlerini kullanacağız.
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

### Ayrıca bakınız

* property [ExportListLabels](../htmlsaveoptions/exportlistlabels/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
