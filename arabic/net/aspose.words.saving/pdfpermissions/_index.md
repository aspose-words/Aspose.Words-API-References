---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.PdfPermissions للتحكم في وصول المستخدمين إلى ملفات PDF المشفرة. حسّن الأمان وأدر عمليات المستندات بفعالية.
type: docs
weight: 6310
url: /ar/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر.

```csharp
[Flags]
public enum PdfPermissions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| DisallowAll | `0` | لا يسمح بجميع العمليات على مستند PDF. هذه هي القيمة الافتراضية. |
| AllowAll | `FFFF` | يسمح بإجراء كافة العمليات على مستند PDF. |
| ContentCopy | `10` | نسخ أو استخراج النصوص والرسومات من المستند بطريقة أخرى من خلال عمليات أخرى غير تلك التي يتم التحكم فيها بواسطة ContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | استخراج النصوص والرسومات (لدعم إمكانية الوصول للمستخدمين ذوي الإعاقة أو لأغراض أخرى). |
| ModifyContents | `8` | تعديل محتويات المستند من خلال عمليات أخرى غير تلك التي يتم التحكم فيها بواسطة ModifyAnnotations ،FillIn ، وDocumentAssembly . |
| ModifyAnnotations | `20` | إضافة أو تعديل التعليقات النصية وملء حقول النموذج التفاعلي، وإذاModifyContents يقوم is أيضًا بتعيين أو إنشاء أو تعديل حقول النموذج التفاعلية (بما في ذلك حقول التوقيع). |
| FillIn | `100` | املأ حقول النموذج التفاعلي الموجودة (بما في ذلك حقول التوقيع)، حتى لوModifyContents واضح. |
| DocumentAssembly | `400` | تجميع المستند (إدراج أو تدوير أو حذف الصفحات وإنشاء عناصر مخطط المستند أو الصور المصغرة)، حتى لوModifyContents واضح. |
| Printing | `4` | اطبع المستند (ربما ليس بأعلى مستوى من الجودة، اعتمادًا على ما إذا كان HighResolutionPrinting تم تعيينه أيضًا). |
| HighResolutionPrinting | `804` | اطبع المستند على تمثيل يُمكن من خلاله إنشاء نسخة رقمية دقيقة من محتوى PDF، استنادًا إلى خوارزمية تعتمد على التنفيذ. عند مسح هذا العلم (و)Printing يجب أن تقتصر الطباعة على تمثيل منخفض المستوى للمظهر، ربما بجودة متدهورة. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
