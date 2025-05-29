---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان دعم النص ثنائي الاتجاه مُفعّلاً في خيارات الحقل. أدر تحديثات النصوص بسهولة لتحسين وظائف تعدد اللغات.
type: docs
weight: 150
url: /ar/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

يحصل على القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا أو يعينها.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية على`حقيقي`يتم تنفيذ خطوات إضافية لإنتاج نتيجة حقل متوافقة من اليمين إلى اليسار language (أي العربية أو العبرية) أثناء تحديثها.

عندما يتم تعيين هذه الخاصية على`خطأ شنيع` إذا تم استخدام لغة من اليمين إلى اليسار، فإن صحة حقل result بعد تحديثه غير مضمونة.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية استخدام FieldOptions للتأكد من أن تحديث الحقل يدعم النص ثنائي الاتجاه بشكل كامل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // تأكد من أن أي عملية حقل تتضمن نصًا من اليمين إلى اليسار يتم تنفيذها كما هو متوقع.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// استخدم منشئ المستندات لإدراج حقل يحتوي على النص من اليمين إلى اليسار.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
