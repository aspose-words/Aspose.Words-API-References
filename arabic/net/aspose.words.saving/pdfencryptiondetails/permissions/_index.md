---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية أذونات PdfEncryptionDetails، التي تُحدد عمليات المستخدم على ملفات PDF المشفرة. تمتع بإدارة مستندات آمنة مع إمكانية الوصول القابلة للتخصيص!
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هيDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

## أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// تمديد الأذونات للسماح بتحرير التعليقات التوضيحية.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند، سوف نحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
