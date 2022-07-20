---
title: ImportFormatMode
second_title: Aspose.Words لمراجع .NET API
description: يحدد كيفية دمج التنسيق عند استيراد محتوى من مستند آخر.
type: docs
weight: 3030
url: /ar/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

يحدد كيفية دمج التنسيق عند استيراد محتوى من مستند آخر.

```csharp
public enum ImportFormatMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| UseDestinationStyles | `0` | استخدم أنماط المستند الوجهة وانسخ الأنماط الجديدة. هذا هو الخيار الافتراضي. |
| KeepSourceFormatting | `1` | انسخ جميع الأنماط المطلوبة إلى المستند الوجهة ، وقم بإنشاء أسماء أنماط فريدة إذا لزم الأمر. |
| KeepDifferentStyles | `2` | نسخ الأنماط المختلفة عن تلك الموجودة في المستند المصدر فقط. |

### ملاحظات

عند نسخ عقد من مستند إلى آخر ، يحدد هذا الخيار كيفية حل التنسيق عندما يكون لكلا المستندين نمط يحمل نفس الاسم ، ولكن بتنسيق مختلف.

يتم حل التنسيق على النحو التالي:

1. تتم مطابقة الأنماط المضمنة باستخدام معرف النمط المستقل للإعدادات المحلية . تتم مطابقة الأنماط المعرفة من قبل المستخدم باستخدام اسم نمط حساس لحالة الأحرف.
2. إذا لم يتم العثور على نمط مطابق في المستند الوجهة ، فسيتم نسخ style (وجميع الأنماط المشار إليها بواسطته) في الوثيقة الوجهة document ويتم تحديث العقد المستوردة للإشارة إلى النمط الجديد.
3. في حالة وجود نمط مطابق بالفعل في المستند الوجهة ، فإن ما يحدث_ x000d_ يعتمد على ملف`importFormatMode` تم تمرير المعلمة to [`الوثيقة. عقد الاستيراد`](../documentbase/importnode) كما هو موضح أدناه.

عند استخدام ملف **UseDestinationStyles**الخيار ، إذا كان النمط المطابق موجودًا بالفعل في المستند الوجهة ، فلن يتم نسخ النمط ويتم تحديث العقد المستوردة للإشارة إلى النمط الحالي.

عيب استخدام **UseDestinationStyles** هو أن النص الذي تم استيراده قد يبدو مختلفًا في المستند الوجهة مقارنة بالمستند المصدر ._ x000d_ على سبيل المثال ، يستخدم نمط "العنوان 1" في المستند المصدر الخط Arial 16pt و_ x000d_ نمط "العنوان 1" في المستند الوجهة يستخدم Times New خط Roman 14pt. عند استيراد نص من نمط "العنوان 1" بدون تنسيق مباشر آخر ، فإنه سيظهر كخط Times New Roman 14pt في المستند الوجهة.

**الاحتفاظ بتنسيق المصدر**يسمح الخيار بالتأكد من أن المحتوى الذي تم استيراده يبدو بنفس في المستند الوجهة كما يبدو في المستند المصدر ._ x000d_ إذا كان هناك نمط مطابق بالفعل في المستند الوجهة ، فسيتم توسيع تنسيق نمط المصدر إلى سمات العقدة المباشرة ويكون النمط هو تم تغييره إلى عادي . إذا لم يكن النمط موجودًا في المستند الوجهة ، فسيتم استيراد نمط المصدر إلى المستند الوجهة وتطبيقه على العقدة المستوردة. غير موجود في المستند الوجهة. في هذه الحالة سيتم توسيع تنسيق هذا النمط إلى سمات العقدة المباشرة لصالح الحفاظ على تنسيق العقدة الأصلي.

عيب استخدام **الاحتفاظ بتنسيق المصدر**هو أنه إذا قمت بإجراء العديد من عمليات الاستيراد ، فقد ينتهي بك الأمر بالعديد من الأنماط في المستند الوجهة وهذا قد يجعل استخدام تنسيق نمط متناسق في Microsoft Word أمرًا صعبًا بالنسبة لهذا المستند.

استخدام **KeepDifferentStyles** يسمح الخيار بإعادة استخدام أنماط الوجهة إذا كان التنسيق الذي توفره مطابقًا للأنماط الموجودة في المستند المصدر ._ x000d_ إذا كان النمط في المستند الوجهة مختلفًا عن المصدر ، فسيتم استيراده.

### أمثلة

يوضح كيفية إدراج مستند في مستند آخر.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->