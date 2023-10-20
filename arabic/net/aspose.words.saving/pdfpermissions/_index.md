---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfPermissions تعداد. يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر في C#.
type: docs
weight: 5510
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
| DisallowAll | `0` | عدم السماح بجميع العمليات على مستند PDF. هذه هي القيمة الافتراضية. |
| AllowAll | `FFFF` | يسمح بجميع العمليات على مستند PDF. |
| ContentCopy | `10` | نسخ أو استخراج النص والرسومات من المستند عن طريق عمليات أخرى غير تلك التي يتم التحكم بها بواسطة ContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | استخراج النصوص والرسومات (لدعم إمكانية الوصول للمستخدمين ذوي الإعاقة أو لأغراض أخرى). |
| ModifyContents | `8` | تعديل محتويات الوثيقة بعمليات أخرى غير تلك التي يتحكم فيها ModifyAnnotations ,FillIn ، وDocumentAssembly . |
| ModifyAnnotations | `20` | إضافة التعليقات التوضيحية النصية أو تعديلها، وملء حقول النماذج التفاعلية، وإذاModifyContents is يقوم أيضًا بتعيين أو إنشاء أو تعديل حقول النموذج التفاعلية (بما في ذلك حقول التوقيع). |
| FillIn | `100` | املأ حقول النموذج التفاعلي الموجودة (بما في ذلك حقول التوقيع)، حتى لوModifyContents واضح. |
| DocumentAssembly | `400` | قم بتجميع المستند (إدراج الصفحات أو تدويرها أو حذفها وإنشاء عناصر مخطط تفصيلي للمستند أو صور مصغرة )، حتى لوModifyContents واضح. |
| Printing | `4` | طباعة المستند (ربما ليس على أعلى مستوى من الجودة، اعتمادًا على ما إذا كان HighResolutionPrinting تم ضبطه أيضًا). |
| HighResolutionPrinting | `804` | اطبع المستند إلى تمثيل يمكن من خلاله إنشاء نسخة رقمية صحيحة من محتوى PDF ، بناءً على خوارزمية تعتمد على التنفيذ. عندما تكون هذه العلامة واضحة (and Printing تم تعيينه)، يجب أن تقتصر الطباعة على تمثيل منخفض المستوى للمظهر، ربما ذو جودة متدهورة. |

## أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// توسيع الأذونات للسماح بتحرير التعليقات التوضيحية.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند، سنحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
