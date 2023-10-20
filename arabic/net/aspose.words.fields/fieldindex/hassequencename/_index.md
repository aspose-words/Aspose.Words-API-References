---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: Aspose.Words لـ .NET
description: FieldIndex HasSequenceName ملكية. يحصل على قيمة تشير إلى ما إذا كان ينبغي استخدام التسلسل أثناء بناء نتيجة الحقل في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

يحصل على قيمة تشير إلى ما إذا كان ينبغي استخدام التسلسل أثناء بناء نتيجة الحقل.

```csharp
public bool HasSequenceName { get; }
```

## أمثلة

يوضح كيفية تقسيم مستند إلى أجزاء من خلال دمج حقول INDEX وSEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE لها نفس القيمة في خاصية "النص" الخاصة بها،
// سيقوم حقل INDEX بتجميعها في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// في خاصية SequenceName، قم بتسمية تسلسل حقل SEQ. سيتم الآن أيضًا عرض كل إدخال في حقل INDEX هذا
// الرقم الذي يوجد عليه عدد التسلسل في موقع حقل XE الذي أنشأ هذا الإدخال.
index.SequenceName = "MySequence";

// قم بتعيين النص الذي يدور حول التسلسل وأرقام الصفحات لشرح معناها للمستخدم.
// سيعرض الإدخال الذي تم إنشاؤه باستخدام هذا التكوين شيئًا مثل "MySequence at 1 on page 1" في رقم الصفحة الخاص به.
// لا يمكن أن يزيد طول PageNumberSeparator وSequenceSeparator عن 15 حرفًا.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" الخاصة بحقل SEQ.
// أدخل حقل SEQ الذي ينقل تسلسل "MySequence" إلى 1.
// لا يختلف هذا الحقل عن نص المستند العادي. ولن يظهر في جدول محتويات حقل INDEX.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// أدخل حقل XE الذي سيؤدي إلى إنشاء إدخال في حقل INDEX.
// نظرًا لأن "MySequence" يقع عند 1 وحقل XE هذا موجود في الصفحة 2، بالإضافة إلى الفواصل المخصصة التي حددناها أعلاه،
// سيعرض إدخال INDEX لهذا الحقل "Cat" على الجانب الأيسر، و"MySequence at 1 on page 2" على اليمين.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// أدخل فاصل صفحات واستخدم حقول SEQ لتقديم "MySequence" إلى 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// أدخل حقل XE بنفس خاصية النص الموجودة أعلاه.
// سيقوم إدخال INDEX بتجميع حقول XE ذات القيم المطابقة في خاصية "النص".
// في إدخال واحد بدلاً من عمل إدخال لكل حقل XE.
// نظرًا لأننا في الصفحة 2 مع "MySequence" في 3، فسيتم إلحاق "، 3 في الصفحة 3" بنفس مُدخل INDEX كما هو مذكور أعلاه.
// سيعرض الآن جزء رقم الصفحة من إدخال INDEX هذا "MySequence at 1 on page 2, 3 on page 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// أدخل حقل XE بقيمة خاصية نصية جديدة وفريدة من نوعها.
// سيؤدي هذا إلى إضافة إدخال جديد، مع MySequence في 3 في الصفحة 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### أنظر أيضا

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
