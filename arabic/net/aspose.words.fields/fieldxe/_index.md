---
title: FieldXE
second_title: Aspose.Words لمراجع .NET API
description: تنفذ حقل XE .
type: docs
weight: 2450
url: /ar/net/aspose.words.fields/fieldxe/
---
## FieldXE class

تنفذ حقل XE .

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype/) { get; set; } | الحصول على نوع إدخال فهرس أو تعيينه. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم تطبيق تنسيق غامق على رقم صفحة الإدخال. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم تطبيق تنسيق مائل على رقم صفحة الإدخال. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement/) { get; set; } | الحصول على أو تعيين النص المستخدم بدلاً من رقم الصفحة. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname/) { get; set; } | الحصول على أو تعيين اسم الإشارة المرجعية التي تحدد نطاقًا من الصفحات المدرجة كرقم صفحة الإدخال. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Text](../../aspose.words.fields/fieldxe/text/) { get; set; } | الحصول على نص الإدخال أو تعيينه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |
| [Yomi](../../aspose.words.fields/fieldxe/yomi/) { get; set; } | الحصول على أو تعيين yomi (الحرف الصوتي الأول لفهارس الفرز) لمدخل الفهرس |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يحدد النص ورقم الصفحة لإدخال الفهرس ، والذي يتم استخدامه بواسطة حقل INDEX.

### أمثلة

يوضح كيفية إنشاء حقل INDEX ، ثم استخدام حقول XE لملئه بالإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة الخاصية Text لحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها ،
// سيجمعها الحقل INDEX في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// تكوين الحقل INDEX فقط لعرض حقول XE الموجودة داخل الحدود
// من إشارة مرجعية مسماة "MainBookmark" ، وخصائصها "EntryType" لها قيمة "A".
// بالنسبة لكل من الحقول INDEX و XE ، تستخدم الخاصية "EntryType" فقط الحرف الأول من قيمة السلسلة الخاصة بها.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// في صفحة جديدة ، ابدأ الإشارة المرجعية باسم يطابق القيمة
// من خاصية "BookmarkName" للحقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// سوف يلتقط حقل INDEX هذا الإدخال لأنه داخل الإشارة المرجعية ،
// ونوع الإدخال الخاص به يتطابق أيضًا مع نوع إدخال الحقل INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// أدخل حقل XE لن يظهر في الفهرس لأن أنواع الإدخال غير متطابقة.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// قم بإنهاء الإشارة المرجعية وأدخل حقل XE بعد ذلك.
// إنه من نفس نوع الحقل INDEX ، لكنه لن يظهر
// لأنه خارج حدود الإشارة المرجعية.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

يوضح كيفية تعبئة حقل INDEX بإدخالات باستخدام حقول XE ، وكذلك تعديل مظهره.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية نص حقل XE على الجانب الأيسر ،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها ،
// سيجمعها الحقل INDEX في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// سيؤدي تعيين قيمة هذه الخاصية على "A" إلى تجميع جميع الإدخالات حسب الحرف الأول ،
// ووضع هذا الحرف بأحرف كبيرة فوق كل مجموعة.
index.Heading = "A";

// قم بتعيين الجدول الذي تم إنشاؤه بواسطة الحقل INDEX ليمتد على عمودين.
index.NumberOfColumns = "2";

// قم بتعيين أي إدخالات بأحرف بداية خارج نطاق أحرف "ac" ليتم حذفها.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// سيظهر حقلا XE التاليان تحت العنوان "A" ،
// مع أنماط النص الخاصة بهم تنطبق أيضًا على أرقام صفحاتهم.
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

// سيكون كلا حقلي XE التاليين تحت عنوان "B" و "C" في جدول محتويات حقول INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX الحقول تفرز جميع المدخلات أبجديًا ، لذلك سيظهر هذا الإدخال تحت "A" مع الاثنين الآخرين.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// لن يظهر هذا الإدخال لأنه يبدأ بالحرف "D" ،
// الذي يقع خارج نطاق الأحرف "ac" الذي تحدده خاصية LetterRange للحقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
