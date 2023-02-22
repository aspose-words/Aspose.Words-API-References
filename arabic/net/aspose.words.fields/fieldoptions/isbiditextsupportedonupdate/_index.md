---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### ملاحظات

عندما يتم تعيين هذه الخاصية على **حقيقي**، يتم تنفيذ خطوات إضافية لإنتاج نتيجة حقل متوافقة مع لغة من اليمين إلى اليسار (أي العربية أو العبرية) أثناء التحديث.

عندما يتم تعيين هذه الخاصية على **خاطئة** ويتم استخدام لغة من اليمين إلى اليسار ، ولا يتم ضمان صحة الحقل result بعد تحديثه.

النظام الأساسي **خاطئة**.

### أمثلة

يوضح كيفية استخدام FieldOptions للتأكد من أن تحديث الحقل يدعم بشكل كامل النص ثنائي الاتجاه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تأكد من أن أي عملية ميدانية تتضمن نصًا من اليمين إلى اليسار يتم تنفيذها على النحو المتوقع. 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// استخدم منشئ المستندات لإدراج حقل يحتوي على النص من اليمين إلى اليسار.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


