---
title: TxtTrailingSpacesOptions Enum
linktitle: TxtTrailingSpacesOptions
articleTitle: TxtTrailingSpacesOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Loading.TxtTrailingSpacesOptions تعداد. يحدد الخيارات المتاحة لمعالجة المسافات الزائدة أثناء الاستيراد منText ملف في C#.
type: docs
weight: 3740
url: /ar/net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

يحدد الخيارات المتاحة لمعالجة المسافات الزائدة أثناء الاستيراد منText ملف.

```csharp
public enum TxtTrailingSpacesOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Trim | `0` |  |
| Preserve | `1` |  |

## أمثلة

يوضح كيفية قطع المسافة البيضاء عند تحميل مستندات النص العادي.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// قم بتعيين خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Preserve"
// للاحتفاظ بجميع أحرف المسافة البيضاء في بداية كل سطر.
// قم بتعيين خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.ConvertToIndent"
// لإزالة كافة الأحرف البيضاء من بداية كل سطر،
// ثم قم بتطبيق مسافة بادئة للسطر الأول الأيسر على الفقرة لمحاكاة تأثير المسافات البيضاء.
// قم بتعيين خاصية "LeadingSpacesOptions" على "TxtLeadingSpacesOptions.Trim"
// لإزالة كافة الأحرف البيضاء من بداية كل سطر.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// قم بتعيين خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Preserve"
 // للاحتفاظ بجميع أحرف المسافة البيضاء في نهاية كل سطر.
 // قم بتعيين خاصية "TrailingSpacesOptions" على "TxtTrailingSpacesOptions.Trim" إلى
// قم بإزالة كافة الأحرف البيضاء من نهاية كل سطر.
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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
