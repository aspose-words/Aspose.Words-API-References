---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية HtmlSaveOptions ExportDropDownFormFieldAsText تصديرات HTML/MHTML من خلال التحكم في تنسيقات حقول القائمة المنسدلة. حسّن مستنداتك!
type: docs
weight: 130
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

يتحكم في كيفية حفظ حقول النموذج المنسدل في HTML أو MHTML. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## ملاحظات

عند ضبطه على`حقيقي` ، يصدر حقول النموذج المنسدلة كنص عادي. عندما`خطأ شنيع`، يتم تصدير حقول النموذج المنسدلة كعنصر SELECT في HTML.

عند التصدير إلى EPUB، يتم دائمًا حفظ حقول نموذج القائمة المنسدلة النصية كنص due وفقًا لمتطلبات هذا التنسيق.

## أمثلة

يوضح كيفية جعل حقول نموذج المربع المنسدل تتداخل مع نص الفقرة عند الحفظ في HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج مربع مجموعة مع تحديد القيمة "اثنين".
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// يسمح لنا علم "ExportDropDownFormFieldAsText" الخاص بكائن SaveOptions هذا بـ
// التحكم في كيفية معالجة مربعات القائمة المنسدلة عند حفظ المستند في HTML.
// تعيينه على "صحيح" سيؤدي إلى تحويل كل مربع منسدل إلى نص بسيط
// الذي يعرض القيمة المحددة حاليًا في المربع المنسدل، مما يؤدي إلى تجميدها فعليًا.
// سيؤدي تعيينه على "false" إلى الحفاظ على وظيفة المربع المنسدل باستخدام علامتي <select> و<option>.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
