---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: خاصية نص "اقتباس الحقل". استرجاع أو تعيين نص بسهولة لتحسين إدارة البيانات. بسّط سير عملك مع هذه الميزة الفعّالة!
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

يحصل على النص الذي سيتم استرداده أو يعينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يظهر كيفية استخدام حقل الاقتباس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج حقل QUOTE، والذي سيعرض قيمة خاصية النص الخاصة به.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// أدخل حقل QUOTE وقم بتضمين حقل DATE بداخله.
// تقوم حقول التاريخ بتحديث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// سيؤدي تعشيش حقل DATE داخل حقل QUOTE على هذا النحو إلى تجميد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// قم بتحديث كافة الحقول لعرض نتائجها الصحيحة.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### أنظر أيضا

* class [FieldQuote](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
