---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء التحديث الميداني أم لا.
type: docs
weight: 150
url: /ar/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء التحديث الميداني أم لا.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### ملاحظات

عندما يتم تعيين هذه الخاصية إلى`حقيقي`، يتم تنفيذ خطوات إضافية لإنتاج نتيجة حقل متوافقة من اليمين إلى اليسار language (أي العربية أو العبرية) أثناء تحديثها.

عندما يتم تعيين هذه الخاصية إلى`خطأ شنيع` ويتم استخدام لغة من اليمين إلى اليسار، ولا يمكن ضمان صحة الحقل result بعد تحديثه.

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

يوضح كيفية استخدام FieldOptions للتأكد من أن تحديث الحقل يدعم بشكل كامل النص ثنائي الاتجاه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // تأكد من أن أي عملية ميدانية تتضمن نصًا من اليمين إلى اليسار يتم تنفيذها كما هو متوقع.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// استخدم منشئ المستندات لإدراج حقل يحتوي على نص من اليمين إلى اليسار.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


