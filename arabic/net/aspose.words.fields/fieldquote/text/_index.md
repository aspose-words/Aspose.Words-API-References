---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: FieldQuote Text ملكية. الحصول على النص أو تعيينه لاسترداده في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

الحصول على النص أو تعيينه لاسترداده.

```csharp
public string Text { get; set; }
```

## أمثلة

يظهر كيفية استخدام حقل عرض الأسعار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل عرض أسعار، والذي سيعرض قيمة خاصية النص الخاصة به.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// أدخل حقل عرض أسعار وقم بدمج حقل التاريخ بداخله.
// تقوم حقول التاريخ بتحديث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// سيؤدي تداخل حقل التاريخ داخل حقل عرض الأسعار بهذه الطريقة إلى تجميد قيمته
// حتى التاريخ الذي أنشأنا فيه المستند.
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
