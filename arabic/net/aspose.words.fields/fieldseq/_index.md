---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldSeq فصل. ينفذ حقل SEQ في C#.
type: docs
weight: 2390
url: /ar/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

ينفذ حقل SEQ.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldSeq : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | الحصول على أو تعيين اسم الإشارة المرجعية التي تشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج رقم التسلسل التالي للعنصر المحدد. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | الحصول على رقم صحيح يمثل مستوى العنوان أو تعيينه لإعادة تعيين الرقم التسلسلي إليه. إرجاع -1 إذا كان الرقم غائبًا. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | الحصول على رقم صحيح أو تعيينه لإعادة تعيين الرقم التسلسلي إليه. يُرجع -1 إذا كان الرقم غائبًا. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | الحصول على أو تعيين الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

ترقيم الفصول والجداول والأشكال وقوائم العناصر الأخرى المحددة من قبل المستخدم في المستند بشكل تسلسلي.

## أمثلة

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" الخاصة بحقل SEQ.
// أدخل حقل SEQ الذي سيعرض قيمة العد الحالية لـ "MySequence"،
// بعد استخدام خاصية "ResetNumber" لتعيينها على 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// اعرض الرقم التالي في هذا التسلسل مع حقل SEQ آخر.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// أدخل عنوان المستوى 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// أدخل حقل SEQ آخر من نفس التسلسل وقم بتكوينه لإعادة تعيين العدد في كل عنوان بـ 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// العنوان أعلاه هو عنوان المستوى 1، لذا تتم إعادة تعيين عدد هذا التسلسل إلى 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// انتقل إلى الرقم التالي من هذا التسلسل.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

يوضح كيفية الجمع بين جدول المحتويات وحقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول محتوياته لكل حقل تسلسلي موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل SEQ،
// ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// قم بتكوين حقل جدول المحتويات هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// قم بتكوين حقل جدول المحتويات هذا لالتقاط حقول SEQ الموجودة ضمن حدود الإشارة المرجعية فقط
// اسمه "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" الخاصة بحقل SEQ.
// أدخل حقل SEQ الذي يحتوي على معرف تسلسل يطابق جدول المحتويات
// خاصية TableOfFigersLabel. لن يقوم هذا الحقل بإنشاء إدخال في جدول المحتويات لأنه موجود بالخارج
// حدود الإشارة المرجعية المعينة بواسطة "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFigursLabel" الخاصة بجدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// ستظهر الفقرة التي تحتوي على هذا الحقل في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// تسلسل حقل SEQ هذا لا يتطابق مع خاصية "TableOfFigersLabel" الخاصة بجدول المحتويات،
// ويقع ضمن حدود الإشارة المرجعية. لن تظهر فقرتها في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFigersLabel" الخاصة بجدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. ستظهر محتويات تلك الإشارة المرجعية في إدخال جدول المحتويات لحقل التسلسل هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات نظرًا لأن حقل SEQ أعلاه يشير إليها.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

يوضح كيفية ملء حقل جدول المحتويات بالإدخالات باستخدام حقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول محتوياته لكل حقل تسلسلي موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تتضمن حقل التسلسل ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" الخاصة بحقل SEQ.
// استخدم خاصية "TableOfFigersLabel" لتسمية التسلسل الرئيسي لجدول المحتويات.
// الآن، سيقوم جدول المحتويات هذا فقط بإنشاء إدخالات من حقول SEQ مع تعيين "SequenceIdentifier" الخاص بها على "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
 لن تقوم حقول SEQ من تسلسل البادئة هذا بإنشاء إدخالات جدول المحتويات.
// كل إدخال جدول محتويات تم إنشاؤه من حقل SEQ للتسلسل الرئيسي سيعرض الآن أيضًا العدد الذي
// تسلسل البادئة قيد التشغيل حاليًا في حقل SEQ للتسلسل الأساسي الذي قام بالإدخال.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// سيعرض كل إدخال في جدول المحتويات عدد تسلسل البادئة على الفور إلى اليسار
// رقم الصفحة التي يظهر عليها حقل التسلسل الرئيسي.
// يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// هناك طريقتان لاستخدام حقول التسلسل لملء جدول المحتويات هذا.
// 1 - إدراج حقل SEQ ينتمي إلى تسلسل بادئة جدول المحتويات:
// سيؤدي هذا الحقل إلى زيادة عدد تسلسل SEQ لـ "PrefixSequence" بمقدار 1.
// نظرًا لأن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
// بواسطة خاصية "TableOfFigersLabel" لجدول المحتويات، لن يظهر كإدخال.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - إدراج حقل SEQ ينتمي إلى التسلسل الرئيسي لجدول المحتويات:
// سيقوم حقل SEQ هذا بإنشاء إدخال في جدول المحتويات.
// سيحتوي إدخال جدول المحتويات على الفقرة التي يوجد بها حقل التسلسل ورقم الصفحة التي يظهر عليها.
// سيعرض هذا الإدخال أيضًا العدد الذي يوجد به تسلسل البادئة حاليًا،
// مفصولة عن رقم الصفحة بالقيمة الموجودة في خاصية SeqenceSeparator الخاصة بجدول المحتويات.
// عدد "PrefixSequence" هو 1، هذا الحقل SEQ للتسلسل الرئيسي موجود في الصفحة 2،
// والفاصل هو ">"، لذلك سيعرض الإدخال "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// أدخل صفحة، وقم بتقديم تسلسل البادئة بمقدار 2، وأدخل حقل SEQ لإنشاء إدخال جدول المحتويات بعد ذلك.
// تسلسل البادئة الآن عند 2، وحقل التسلسل الرئيسي SEQ موجود في الصفحة 3،
// لذلك سيعرض إدخال جدول المحتويات "2>3" في عدد الصفحات الخاص به.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
