---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية HtmlFixedSaveOptions ExportFormFields على تعزيز تصدير المستندات من خلال الحفاظ على تفاعلية حقول النموذج، مما يؤدي إلى تحسين تجربة المستخدم.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

يحصل على أو يعين مؤشرًا حول ما إذا كانت حقول النموذج يتم تصديرها كعناصر interactive (كعلامة "إدخال") بدلاً من تحويلها إلى نص أو رسومات.

```csharp
public bool ExportFormFields { get; set; }
```

## أمثلة

يوضح كيفية تصدير حقول النموذج إلى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// عندما نقوم بتصدير مستند يحتوي على حقول نموذج إلى .html،
// هناك طريقتان يمكن لـ Aspose.Words من خلالهما تصدير حقول النموذج.
// سيؤدي تعيين علامة "ExportFormFields" إلى "true" إلى تصديرها ككائنات تفاعلية.
// سيؤدي تعيين هذا العلم إلى "خطأ" إلى عرض حقول النموذج كنص عادي.
// سيؤدي هذا إلى تجميدها عند قيمتها الحالية، ومنع قارئ مستند HTML الخاص بنا
// من القدرة على التفاعل معهم.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
