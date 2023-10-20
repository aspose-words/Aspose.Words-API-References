---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Range فصل. يمثل منطقة متجاورة في المستند في C#.
type: docs
weight: 4520
url: /ar/net/aspose.words/range/
---
## Range class

يمثل منطقة متجاورة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع النطاقات](https://docs.aspose.com/words/net/working-with-ranges/) مقالة توثيقية.

```csharp
public class Range
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | إرجاع أ[`Bookmarks`](./bookmarks/) المجموعة التي تمثل جميع الإشارات المرجعية في النطاق. |
| [Fields](../../aspose.words/range/fields/) { get; } | إرجاع أ[`Fields`](./fields/) المجموعة التي تمثل جميع الحقول في النطاق. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | إرجاع أ[`FormFields`](./formfields/) المجموعة التي تمثل جميع حقول النموذج في النطاق. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | الحصول على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا النطاق. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | إرجاع أ[`StructuredDocumentTags`](./structureddocumenttags/) المجموعة التي تمثل جميع علامات المستندات المنظمة في النطاق. |
| [Text](../../aspose.words/range/text/) { get; } | يحصل على نص النطاق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | حذف كافة أحرف النطاق. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | تغيير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | يستبدل كافة تكرارات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | يستبدل كافة تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | يستبدل كافة تكرارات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | يستبدل كافة تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [ToDocument](../../aspose.words/range/todocument/)() | إنشاء مستند جديد كامل التكوين يحتوي على النطاق. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | إلغاء ربط الحقول في هذا النطاق. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | يقوم بتحديث قيم حقول المستند في هذا النطاق. |

## ملاحظات

يتم تمثيل المستند بواسطة شجرة من العقد وتوفر العقد عمليات للعمل مع الشجرة، ولكن يكون تنفيذ بعض العمليات أسهل إذا تم التعامل مع document كتسلسل متجاور من النص.

`Range`هي واجهة "واجهة" توفر أساليب تتعامل مع document أو أجزاء من المستند كنص "مسطح" بغض النظر عن حقيقة أن عقد document مخزنة في نموذج كائن يشبه الشجرة.

`Range` لا يحتوي على أي نص أو عقد، فهو مجرد عرض أو "نافذة" على جزء من المستند.

## أمثلة

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
