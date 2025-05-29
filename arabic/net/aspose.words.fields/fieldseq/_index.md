---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldSeq لتطبيق سلس لحقول SEQ. حسّن أتمتة مستنداتك بميزات قوية ومرونة عالية.
type: docs
weight: 2800
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
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | يحصل على اسم إشارة مرجعية أو يعينه بحيث يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج رقم التسلسل التالي للعنصر المحدد. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | يحصل على أو يعين رقمًا صحيحًا يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. يعيد -1 إذا كان الرقم غائبًا. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | يحصل على أو يعيّن عددًا صحيحًا لإعادة تعيين الرقم التسلسلي إليه. يُرجع -1 إذا كان الرقم غير موجود. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | يحصل على الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها أو يعينه. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

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

ترقيم الفصول والجداول والأشكال وقوائم العناصر الأخرى التي يحددها المستخدم في المستند بشكل تسلسلي.

## أمثلة

يُظهر إنشاء الترقيم باستخدام حقول SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعرض حقول SEQ عددًا يتزايد عند كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بعدد منفصل لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" في حقل SEQ.
// أدخل حقل SEQ الذي سيعرض قيمة العدد الحالية لـ "MySequence"،
// بعد استخدام خاصية "ResetNumber" لتعيينها إلى 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// عرض الرقم التالي في هذا التسلسل باستخدام حقل SEQ آخر.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

//إدراج عنوان المستوى 1.
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

// العنوان أعلاه هو عنوان المستوى 1، لذا يتم إعادة تعيين العدد لهذا التسلسل إلى 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

//الانتقال إلى الرقم التالي من هذا التسلسل.
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

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل تسلسل موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل التسلسل،
// ورقم الصفحة التي يظهر فيها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// قم بتكوين حقل جدول المحتويات هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// قم بتكوين حقل جدول المحتويات هذا لالتقاط حقول التسلسل فقط التي تقع ضمن حدود الإشارة المرجعية
// اسمه "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// تعرض حقول SEQ عددًا يتزايد عند كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بعدد منفصل لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" في حقل SEQ.
// أدخل حقل SEQ الذي يحتوي على معرف تسلسل يتطابق مع جدول المحتويات
// خاصية TableOfFiguresLabel. لن يُنشئ هذا الحقل إدخالاً في جدول المحتويات لأنه خارج
// حدود الإشارة المرجعية المحددة بواسطة "BookmarkName".
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

// لا يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات،
// ويقع ضمن حدود الإشارة المرجعية. لن تظهر فقرته في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. سيظهر محتوى هذه الإشارة المرجعية في مُدخل جدول المحتويات لحقل التسلسل هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات بسبب وجود حقل SEQ أعلاه يشير إليه.
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

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل تسلسل موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تتضمن حقل SEQ ورقم الصفحة التي يظهر فيها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// تعرض حقول SEQ عددًا يتزايد عند كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بعدد منفصل لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" في حقل SEQ.
// استخدم خاصية "TableOfFiguresLabel" لتسمية التسلسل الرئيسي لجدول المحتويات.
// الآن، سيقوم جدول المحتويات هذا بإنشاء إدخالات فقط من حقول التسلسل مع تعيين "SequenceIdentifier" الخاصة بها على "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
 // لن تقوم حقول SEQ من تسلسل البادئة هذا بإنشاء إدخالات TOC.
// كل إدخال جدول المحتويات الذي تم إنشاؤه من حقل التسلسل الرئيسي سيعرض الآن أيضًا العدد الذي
// تسلسل البادئة موجود حاليًا في حقل تسلسل SEQ الأساسي الذي أجرى الإدخال.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// سيعرض كل إدخال في جدول المحتويات عدد تسلسل البادئة على الفور إلى اليسار
// رقم الصفحة التي يظهر فيها حقل التسلسل الرئيسي.
//يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// هناك طريقتان لاستخدام حقول SEQ لملء جدول المحتويات هذا.
// 1 - إدراج حقل SEQ الذي ينتمي إلى تسلسل بادئة جدول المحتويات:
// سيؤدي هذا الحقل إلى زيادة عدد تسلسل SEQ لـ "PrefixSequence" بمقدار 1.
// بما أن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
// بواسطة خاصية "TableOfFiguresLabel" في جدول المحتويات، فلن يظهر كإدخال.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - إدراج حقل SEQ الذي ينتمي إلى التسلسل الرئيسي لجدول المحتويات:
// سيؤدي حقل SEQ هذا إلى إنشاء إدخال في جدول المحتويات.
// سيحتوي إدخال جدول المحتويات على الفقرة التي يوجد بها حقل التسلسل ورقم الصفحة التي يظهر فيها.
// سيعرض هذا الإدخال أيضًا العدد الذي يوجد عنده تسلسل البادئة حاليًا،
// مفصولة عن رقم الصفحة بالقيمة الموجودة في خاصية SeqenceSeparator في جدول المحتويات.
// عدد "PrefixSequence" هو 1، حقل SEQ التسلسل الرئيسي هذا موجود في الصفحة 2،
// والفاصل هو ">"، لذلك سيتم عرض الإدخال "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// قم بإدراج صفحة، ثم قم بتقديم تسلسل البادئة بمقدار 2، ثم أدخل حقل SEQ لإنشاء إدخال جدول المحتويات بعد ذلك.
// تسلسل البادئة موجود الآن عند 2، وحقل تسلسل SEQ الرئيسي موجود في الصفحة 3،
// لذلك سيتم عرض إدخال جدول المحتويات "2>3" في عدد الصفحات.
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
