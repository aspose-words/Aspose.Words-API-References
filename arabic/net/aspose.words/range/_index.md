---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Range، مفتاحك لإدارة أقسام المستندات بسهولة. حسّن معالجة مستنداتك بتحكم سلس ومرونة.
type: docs
weight: 5250
url: /ar/net/aspose.words/range/
---
## Range class

يمثل منطقة متجاورة في مستند.

لمعرفة المزيد، قم بزيارة[العمل مع النطاقات](https://docs.aspose.com/words/net/working-with-ranges/) مقالة توثيقية.

```csharp
public class Range : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | يعيد[`Bookmarks`](./bookmarks/) مجموعة تمثل جميع الإشارات المرجعية في النطاق. |
| [Fields](../../aspose.words/range/fields/) { get; } | يعيد[`Fields`](./fields/) مجموعة تمثل جميع الحقول في النطاق. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | يعيد[`FormFields`](./formfields/) مجموعة تمثل جميع حقول النموذج في النطاق. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | يحصل على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا النطاق. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | يعيد[`StructuredDocumentTags`](./structureddocumenttags/) مجموعة تمثل جميع علامات المستندات المنظمة في النطاق. |
| [Text](../../aspose.words/range/text/) { get; } | يحصل على نص النطاق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | يحذف جميع أحرف النطاق. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | تغيير قيم نوع الحقل[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../aspose.words.fields/fieldstart/) ،[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ،[`FieldEnd`](../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | يستبدل جميع حالات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | يستبدل جميع حالات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | يستبدل جميع حالات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | يستبدل جميع حالات نمط سلسلة الأحرف المحددة بسلسلة بديلة. |
| [ToDocument](../../aspose.words/range/todocument/)() | يقوم بإنشاء مستند جديد كامل التكوين يحتوي على النطاق. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | إلغاء ربط الحقول في هذا النطاق. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | تحديث قيم حقول المستند في هذا النطاق. |

## ملاحظات

يتم تمثيل المستند بواسطة شجرة من العقد وتوفر العقد العمليات للعمل مع الشجرة، ولكن بعض العمليات يكون من الأسهل إجراؤها إذا تم التعامل مع document كتسلسل متجاور من النص.

`Range` هي واجهة "واجهة" توفر طرقًا تعامل document أو أجزاء من المستند كنص "مسطح" بغض النظر عن حقيقة أن عقد document مخزنة في نموذج كائن يشبه الشجرة.

`Range` لا يحتوي على أي نص أو عقد، فهو مجرد عرض أو "نافذة" فوق جزء من المستند.

## أمثلة

يوضح كيفية الحصول على محتويات النص لجميع العقد التي يغطيها النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
