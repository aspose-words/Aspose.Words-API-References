---
title: Class Range
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Range فصل. يمثل منطقة مجاورة في مستند.
type: docs
weight: 4270
url: /ar/net/aspose.words/range/
---
## Range class

يمثل منطقة مجاورة في مستند.

```csharp
public class Range
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | إرجاع أ[`Bookmarks`](./bookmarks/) المجموعة التي تمثل جميع الإشارات المرجعية في النطاق. |
| [Fields](../../aspose.words/range/fields/) { get; } | إرجاع أ[`Fields`](./fields/) المجموعة التي تمثل جميع الحقول في النطاق. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | إرجاع أ[`FormFields`](./formfields/) المجموعة التي تمثل جميع حقول النموذج في النطاق. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | إرجاع أ[`StructuredDocumentTags`](./structureddocumenttags/) المجموعة التي تمثل جميع علامات المستند المهيكلة في النطاق. |
| [Text](../../aspose.words/range/text/) { get; } | يحصل على نص النطاق . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | حذف كافة أحرف النطاق . |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | يغير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) من[`FieldStart`](../../aspose.words.fields/fieldstart/) و[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) و[`FieldEnd`](../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول. |
| [Replace](../../aspose.words/range/replace/#replace_2)(Regex, string) | يستبدل كل تكرارات نمط الحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace)(string, string) | يستبدل كل تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [Replace](../../aspose.words/range/replace/#replace_3)(Regex, string, FindReplaceOptions) | يستبدل كل تكرارات نمط الحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace_1)(string, string, FindReplaceOptions) | يستبدل كل تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [ToDocument](../../aspose.words/range/todocument/)() | إنشاء مستند جديد كامل التكوين يحتوي على النطاق. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | إلغاء ربط الحقول في هذا النطاق . |
| [UpdateFields](../../aspose.words/range/updatefields/)() | يقوم بتحديث قيم حقول الوثيقة في هذا النطاق. |

### ملاحظات

يتم تمثيل المستند بشجرة من العقد وتوفر العقد Operations للعمل مع الشجرة ، ولكن بعض العمليات يكون من الأسهل تنفيذها إذا تم التعامل مع document كتسلسل نص متجاور.

**نطاق** هي واجهة "واجهة" توفر طرقًا تتعامل مع document أو أجزاء من المستند كنص "مسطح" بغض النظر عن حقيقة أن عُقد document يتم تخزينها في نموذج كائن يشبه الشجرة.

**نطاق** لا يحتوي على أي نص أو عقد ، فهو مجرد عرض أو "نافذة" فوق جزء من المستند.

### أمثلة

يوضح كيفية الحصول على محتويات النص لجميع العقد التي يغطيها النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


