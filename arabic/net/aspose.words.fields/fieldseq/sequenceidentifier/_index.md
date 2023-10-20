---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words لـ .NET
description: FieldSeq SequenceIdentifier ملكية. الحصول على أو تعيين الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

الحصول على أو تعيين الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها.

```csharp
public string SequenceIdentifier { get; set; }
```

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

* class [FieldSeq](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
