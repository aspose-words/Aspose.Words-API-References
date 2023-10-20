---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: Aspose.Words لـ .NET
description: FieldToc PrefixedSequenceIdentifier ملكية. الحصول على أو تعيين معرف التسلسل الذي يجب إضافة بادئة له إلى رقم صفحة الإدخال في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

الحصول على أو تعيين معرف التسلسل الذي يجب إضافة بادئة له إلى رقم صفحة الإدخال.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## أمثلة

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

* class [FieldToc](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
