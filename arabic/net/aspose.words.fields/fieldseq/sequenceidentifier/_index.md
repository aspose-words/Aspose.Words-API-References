---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldSeq SequenceIdentifier لإدارة أسماء سلسلة العناصر وتخصيصها بسهولة لترقيم وتنظيم فعالين.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

يحصل على الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها أو يعينه.

```csharp
public string SequenceIdentifier { get; set; }
```

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

* class [FieldSeq](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
