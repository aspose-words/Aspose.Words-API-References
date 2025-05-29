---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldToc PrefixedSequenceIdentifier—إدارة معرفات التسلسل بكفاءة وتعزيز رقم صفحة الإدخال الخاص بك باستخدام بادئات فريدة.
type: docs
weight: 120
url: /ar/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

يحصل على معرف التسلسل الذي يجب إضافة بادئة له إلى رقم صفحة الإدخال أو يعينه.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## أمثلة

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

* class [FieldToc](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
