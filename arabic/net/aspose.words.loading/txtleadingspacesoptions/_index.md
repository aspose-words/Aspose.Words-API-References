---
title: TxtLeadingSpacesOptions Enum
linktitle: TxtLeadingSpacesOptions
articleTitle: TxtLeadingSpacesOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words TxtLeadingSpacesOptions لإدارة المسافات البادئة بكفاءة عند استيراد ملفات النصوص. حسّن معالجة مستنداتك اليوم!
type: docs
weight: 4180
url: /ar/net/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enumeration

يحدد الخيارات المتاحة للتعامل مع المسافة البادئة أثناء الاستيراد منText الملف.

```csharp
public enum TxtLeadingSpacesOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| ConvertToIndent | `0` | تتم إزالة المسافات البادئة وتحويلها إلى مسافة بادئة يسرى. |
| Trim | `1` | تم تقليص المسافات البادئة |
| Preserve | `2` | يتم الحفاظ على المسافات البادئة. |

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
