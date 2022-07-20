---
title: PdfPermissions
second_title: Aspose.Words لمراجع .NET API
description: يحدد العمليات المسموح بها للمستخدم في مستند PDF مشفر.
type: docs
weight: 5230
url: /ar/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

يحدد العمليات المسموح بها للمستخدم في مستند PDF مشفر.

```csharp
[Flags]
public enum PdfPermissions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| DisallowAll | `0` | عدم السماح بجميع العمليات على مستند PDF . هذه هي القيمة الافتراضية ._ x000d_ |
| AllowAll | `FFFF` | يسمح بجميع العمليات على مستند PDF . |
| ContentCopy | `10` | انسخ النص والرسومات أو استخرجهما بأي طريقة أخرى من المستند عن طريق عمليات أخرى غير تلك التي يتم التحكم فيها بواسطةContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | استخراج النص والرسومات (لدعم إمكانية الوصول للمستخدمين ذوي الاحتياجات الخاصة أو لأغراض أخرى) ._ x000d_ |
| ModifyContents | `8` | تعديل محتويات المستند بعمليات غير تلك التي يتحكم فيها ModifyAnnotations وFillIn ، وDocumentAssembly . |
| ModifyAnnotations | `20` | أضف التعليقات التوضيحية النصية أو عدلها ، واملأ حقول النموذج التفاعلية ، وإذا كانModifyContents is قم أيضًا بتعيين أو إنشاء أو تعديل حقول النموذج التفاعلية (بما في ذلك حقول التوقيع). |
| FillIn | `100` | املأ حقول النموذج التفاعلية الموجودة (بما في ذلك حقول التوقيع) ، حتى لوModifyContents واضح . |
| DocumentAssembly | `400` | قم بتجميع المستند (إدراج أو تدوير أو حذف الصفحات وإنشاء عناصر مخطط المستند أو الصور المصغرة_ x000d_) ، حتى لوModifyContents واضح . |
| Printing | `4` | قم بطباعة المستند (ربما ليس بأعلى مستوى جودة ، اعتمادًا على ما إذا كان HighResolutionPrintingتم تعيينه أيضًا). |
| HighResolutionPrinting | `804` | اطبع المستند إلى تمثيل يمكن من خلاله إنشاء نسخة رقمية موثوقة من محتوى PDF ، استنادًا إلى خوارزمية تعتمد على التنفيذ. عندما تكون هذه العلامة واضحة (و_ x000d_Printing تم تعيينه) ، يجب أن تقتصر الطباعة على تمثيل منخفض المستوى للمظهر ، من المحتمل أن تكون ذات جودة متدهورة. |

### أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// ابدأ برفض جميع الأذونات.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// تمديد الأذونات للسماح بتحرير التعليقات التوضيحية.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند ، سنحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->