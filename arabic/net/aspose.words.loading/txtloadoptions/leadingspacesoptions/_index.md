---
title: TxtLoadOptions.LeadingSpacesOptions
linktitle: LeadingSpacesOptions
articleTitle: LeadingSpacesOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LeadingSpacesOptions في TxtLoadOptions لتخصيص التعامل مع المسافات البادئة. حسّن تحميل نصك باستخدام إعداد ConvertToIndent الافتراضي.
type: docs
weight: 60
url: /ar/net/aspose.words.loading/txtloadoptions/leadingspacesoptions/
---
## TxtLoadOptions.LeadingSpacesOptions property

يحصل على الخيار المفضل للتعامل مع المسافة البادئة أو يعينه. القيمة الافتراضية هيConvertToIndent .

```csharp
public TxtLeadingSpacesOptions LeadingSpacesOptions { get; set; }
```

## أمثلة

يوضح كيفية تقليم المسافات البيضاء عند تحميل مستندات النص العادي.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى منشئ المستند
// لتعديل كيفية تحميل مستند النص العادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// اضبط خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Preserve"
// للحفاظ على جميع أحرف المسافة البيضاء في بداية كل سطر.
// اضبط خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.ConvertToIndent"
// لإزالة جميع أحرف المسافة البيضاء من بداية كل سطر،
// ثم قم بتطبيق المسافة البادئة للسطر الأول الأيسر على الفقرة لمحاكاة تأثير المسافات البيضاء.
// اضبط خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Trim"
// لإزالة جميع أحرف المسافة البيضاء من بداية كل سطر.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// اضبط خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Preserve"
 // للحفاظ على جميع أحرف المسافة البيضاء في نهاية كل سطر.
 // اضبط خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Trim" إلى
// قم بإزالة جميع أحرف المسافة البيضاء من نهاية كل سطر.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### أنظر أيضا

* enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
