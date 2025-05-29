---
title: FieldXE Class
linktitle: FieldXE
articleTitle: FieldXE
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldXE، الحل الأمثل لتطبيق حقول XE بكفاءة في معالجة المستندات. حسّن سير عملك اليوم!
type: docs
weight: 3020
url: /ar/net/aspose.words.fields/fieldxe/
---
## FieldXE class

ينفذ حقل XE.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldXE : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldXE](fieldxe/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype/) { get; set; } | يحصل على نوع إدخال الفهرس أو يعينه. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تطبيق التنسيق الغامق على رقم صفحة الإدخال. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تطبيق التنسيق المائل على رقم صفحة الإدخال. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement/) { get; set; } | يحصل على النص المستخدم بدلاً من رقم الصفحة أو يعينه. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname/) { get; set; } | يحصل على اسم الإشارة المرجعية التي تحدد نطاق الصفحات التي يتم إدراجها كرقم صفحة الإدخال أو يعينه. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Text](../../aspose.words.fields/fieldxe/text/) { get; set; } | يحصل على نص الإدخال أو يعينه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |
| [Yomi](../../aspose.words.fields/fieldxe/yomi/) { get; set; } | يحصل على أو يعين yomi (الحرف الصوتي الأول لفرز الفهارس) لإدخال الفهرس |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يحدد النص ورقم الصفحة لإدخال الفهرس، والذي يستخدمه حقل INDEX.

## أمثلة

يوضح كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE تحتوي على نفس القيمة في خاصية "النص" الخاصة بها،
// سوف يقوم حقل INDEX بتجميعهم في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// قم بتكوين حقل INDEX فقط لعرض حقول XE الموجودة ضمن الحدود
// لإشارة مرجعية تسمى "MainBookmark"، وخصائص "EntryType" الخاصة بها لها قيمة "A".
// بالنسبة لكلا الحقلين INDEX وXE، تستخدم خاصية "EntryType" الحرف الأول فقط من قيمة السلسلة الخاصة بها.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// في صفحة جديدة، ابدأ الإشارة المرجعية باسم يتطابق مع القيمة
// من خاصية "BookmarkName" في حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// سوف يلتقط حقل INDEX هذا الإدخال لأنه موجود داخل الإشارة المرجعية،
// ونوع الإدخال الخاص به يتطابق أيضًا مع نوع إدخال حقل INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// أدخل حقل XE الذي لن يظهر في INDEX لأن أنواع الإدخالات لا تتطابق.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// قم بإنهاء الإشارة المرجعية وإدراج حقل XE بعد ذلك.
// إنه من نفس نوع حقل INDEX، لكنه لن يظهر
// لأنه خارج حدود الإشارة المرجعية.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

يوضح كيفية ملء حقل INDEX بالإدخالات باستخدام حقول XE، وتعديل مظهره أيضًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE تحتوي على نفس القيمة في خاصية "النص" الخاصة بها،
// سوف يقوم حقل INDEX بتجميعهم في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// سيؤدي تعيين قيمة هذه الخاصية إلى "A" إلى تجميع جميع الإدخالات حسب الحرف الأول منها،
// ثم ضع هذا الحرف بأحرف كبيرة فوق كل مجموعة.
index.Heading = "A";

// قم بتعيين الجدول الذي تم إنشاؤه بواسطة حقل INDEX ليمتد على عمودين.
index.NumberOfColumns = "2";

// قم بتعيين أي إدخالات تحتوي على أحرف بداية خارج نطاق الأحرف "ac" ليتم حذفها.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// سيظهر حقلي XE التاليين تحت عنوان "A"،
// مع تطبيق أنماط النصوص الخاصة بهم أيضًا على أرقام صفحاتهم.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

//سيكون كلا الحقلين XE التاليين تحت عنواني "B" و"C" في جدول محتويات حقول INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// تقوم حقول INDEX بفرز جميع الإدخالات أبجديًا، بحيث يظهر هذا الإدخال تحت "A" مع الإدخالين الآخرين.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// لن يظهر هذا الإدخال لأنه يبدأ بالحرف "D"،
// وهو خارج نطاق الأحرف "ac" الذي تحدده خاصية LetterRange في حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
