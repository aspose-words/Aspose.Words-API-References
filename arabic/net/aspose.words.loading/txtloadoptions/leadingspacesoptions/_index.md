---
title: TxtLoadOptions.LeadingSpacesOptions
second_title: Aspose.Words لمراجع .NET API
description: TxtLoadOptions ملكية. الحصول على أو تعيين الخيار المفضل لمعالجة المسافة البادئة. القيمة الافتراضية هيConvertToIndent .
type: docs
weight: 40
url: /ar/net/aspose.words.loading/txtloadoptions/leadingspacesoptions/
---
## TxtLoadOptions.LeadingSpacesOptions property

الحصول على أو تعيين الخيار المفضل لمعالجة المسافة البادئة. القيمة الافتراضية هيConvertToIndent .

```csharp
public TxtLeadingSpacesOptions LeadingSpacesOptions { get; set; }
```

### أمثلة

يوضح كيفية اقتطاع المسافات البيضاء عند تحميل مستندات ذات نص عادي.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// قم بإنشاء كائن "TxtLoadOptions" ، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// تعيين خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Preserve"
// للاحتفاظ بجميع أحرف المسافات البيضاء في بداية كل سطر.
// تعيين خاصية "LeadingSpacesOptions" إلى "TxtLeadingSpacesOptions.ConvertToIndent"
// لإزالة جميع أحرف المسافات البيضاء من بداية كل سطر ،
// ثم قم بتطبيق مسافة بادئة يسرى للسطر الأول على الفقرة لمحاكاة تأثير المسافات البيضاء.
// تعيين خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Trim"
// لإزالة جميع أحرف المسافات البيضاء من بداية كل سطر.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// تعيين خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Preserve"
// للاحتفاظ بجميع أحرف المسافات البيضاء في نهاية كل سطر. 
// قم بتعيين خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Trim" 
// قم بإزالة جميع أحرف المسافات البيضاء من نهاية كل سطر.
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
* مساحة الاسم [Aspose.Words.Loading](../../txtloadoptions/)
* المجسم [Aspose.Words](../../../)


