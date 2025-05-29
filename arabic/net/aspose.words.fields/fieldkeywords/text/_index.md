---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: إدارة كلماتك الرئيسية بسهولة! تمتع بالوصول إلى نص الكلمات الرئيسية وتخصيصه لتحقيق أداء مُحسّن لمحركات البحث وظهور مُحسّن.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

يحصل على نص الكلمات الرئيسية أو يعينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يظهر لإدراج حقل الكلمات الرئيسية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف بعض الكلمات الرئيسية، والتي يشار إليها أيضًا باسم "العلامات" في مستكشف الملفات.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// يعرض حقل الكلمات الرئيسية قيمة هذه الخاصية.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// تعيين قيمة لخاصية النص الخاصة بالحقل،
// ثم سيؤدي تحديث الحقل أيضًا إلى استبدال الخاصية المضمنة المقابلة بالقيمة الجديدة.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### أنظر أيضا

* class [FieldKeywords](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
