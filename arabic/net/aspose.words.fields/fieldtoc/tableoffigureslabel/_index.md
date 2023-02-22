---
title: FieldToc.TableOfFiguresLabel
second_title: Aspose.Words لمراجع .NET API
description: FieldToc ملكية. الحصول على أو تحديد اسم معرف التسلسل المستخدم عند إنشاء جدول الأرقام.
type: docs
weight: 160
url: /ar/net/aspose.words.fields/fieldtoc/tableoffigureslabel/
---
## FieldToc.TableOfFiguresLabel property

الحصول على أو تحديد اسم معرف التسلسل المستخدم عند إنشاء جدول الأرقام.

```csharp
public string TableOfFiguresLabel { get; set; }
```

### أمثلة

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

* class [FieldToc](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldtoc/)
* المجسم [Aspose.Words](../../../)


