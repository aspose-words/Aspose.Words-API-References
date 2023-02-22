---
title: Class FieldSeq
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldSeq فصل. تنفذ حقل SEQ .
type: docs
weight: 2240
url: /ar/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

تنفذ حقل SEQ .

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
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | الحصول على أو تعيين اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج رقم التسلسل التالي للعنصر المحدد. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | الحصول على أو تعيين رقم صحيح يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إلى . إرجاع -1 إذا كان الرقم غائبًا . |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | الحصول على أو تعيين رقم صحيح لإعادة تعيين الرقم التسلسلي إليه. إرجاع -1 إذا كان الرقم غائباً. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | الحصول على أو تعيين الاسم المخصص لسلسلة العناصر المراد ترقيمها . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

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

فصول الأرقام والجداول والأشكال وقوائم العناصر الأخرى المحددة من قبل المستخدم في المستند بشكل تسلسلي.

### أمثلة

يظهر إنشاء الترقيم باستخدام حقول SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// التي تم تحديدها بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدخل حقل SEQ يعرض قيمة العدد الحالية لـ "MySequence" ،
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

// أدخل حقل SEQ آخر من نفس التسلسل وقم بتكوينه لإعادة تعيين العد في كل عنوان بـ 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// العنوان أعلاه هو عنوان من المستوى 1 ، لذلك يتم إعادة تعيين عدد هذا التسلسل إلى 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// الانتقال إلى الرقم التالي من هذا التسلسل.
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

يوضح كيفية دمج جدول المحتويات وحقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل SEQ موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل SEQ ،
// ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// تكوين حقل جدول المحتويات هذا للحصول على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// تكوين حقل جدول المحتويات هذا لاختيار حقول SEQ الموجودة ضمن حدود إشارة مرجعية فقط
// المسمى "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// التي تم تحديدها بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدخل حقل SEQ يحتوي على معرف تسلسل يطابق جدول المحتويات
// خاصية TableOfFiguresLabel. لن يُنشئ هذا الحقل إدخالاً في جدول المحتويات لأنه خارج
// حدود الإشارة المرجعية المعينة بواسطة "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// ستظهر الفقرة التي تحتوي على هذا الحقل في جدول المحتويات كإدخال.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// لا يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ،
// وضمن حدود الإشارة المرجعية. لن تظهر فقرتها في جدول المحتويات كإدخال.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. ستظهر محتويات هذه الإشارة المرجعية في إدخال جدول المحتويات لحقل SEQ هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات بسبب حقل SEQ أعلاه الذي يشير إليه.
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

يوضح كيفية ملء حقل جدول المحتويات بإدخالات باستخدام حقول SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل SEQ موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تتضمن حقل SEQ ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// التي تم تحديدها بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// استخدم خاصية "TableOfFiguresLabel" لتسمية تسلسل رئيسي لجدول المحتويات.
// الآن ، سيقوم جدول المحتويات هذا بإنشاء إدخالات من حقول SEQ فقط مع تعيين "SequenceIdentifier" على "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
 // SEQ من تسلسل البادئة هذا لن تنشئ إدخالات جدول المحتويات.
// كل إدخال جدول محتويات تم إنشاؤه من حقل SEQ للتسلسل الرئيسي سيعرض الآن أيضًا عدد ذلك
// تسلسل البادئة قيد التشغيل حاليًا في حقل تسلسل SEQ الأساسي الذي جعل الإدخال.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// سيعرض كل إدخال في جدول المحتويات عدد تسلسل البادئة على الفور إلى اليسار
// من رقم الصفحة الذي يظهر عليه حقل التسلسل الرئيسي SEQ.
// يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// هناك طريقتان لاستخدام حقول SEQ لملء جدول المحتويات هذا.
// 1 - إدخال حقل SEQ ينتمي إلى تسلسل بادئة جدول المحتويات:
// سيزيد هذا الحقل عدد تسلسل SEQ لـ "PrefixSequence" بمقدار 1.
// بما أن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
// بواسطة خاصية "TableOfFiguresLabel" لجدول المحتويات ، فلن تظهر كإدخال.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - إدخال حقل SEQ الذي ينتمي إلى التسلسل الرئيسي لجدول المحتويات:
// سيُنشئ حقل SEQ هذا إدخالاً في جدول المحتويات.
// سيحتوي إدخال جدول المحتويات على الفقرة التي يوجد بها حقل SEQ ورقم الصفحة التي تظهر عليها.
// سيعرض هذا الإدخال أيضًا عدد تسلسل البادئة حاليًا ،
// مفصولة عن رقم الصفحة بالقيمة في خاصية SeqenceSeparator في جدول المحتويات.
// عدد "PrefixSequence" هو 1 ، هذا التسلسل الرئيسي حقل SEQ موجود في الصفحة 2 ،
// والفاصل هو ">" ، لذا سيعرض الإدخال "1 > 2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// أدخل صفحة ، وقدم تسلسل البادئة بمقدار 2 ، وأدخل حقل SEQ لإنشاء إدخال جدول المحتويات بعد ذلك.
// تسلسل البادئة الآن في 2 ، وحقل التسلسل الرئيسي SEQ موجود في الصفحة 3 ،
// لذلك سيعرض إدخال جدول المحتويات "2 > 3" في عدد صفحاته.
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


