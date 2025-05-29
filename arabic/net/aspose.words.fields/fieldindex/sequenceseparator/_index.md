---
title: FieldIndex.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldIndex SequenceSeparator، وقم بإدارة تسلسلات الأحرف بسهولة لفصل التسلسل وأرقام الصفحات في تطبيقاتك.
type: docs
weight: 160
url: /ar/net/aspose.words.fields/fieldindex/sequenceseparator/
---
## FieldIndex.SequenceSeparator property

يحصل على أو يعين تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات.

```csharp
public string SequenceSeparator { get; set; }
```

## أمثلة

يوضح كيفية تقسيم المستند إلى أجزاء عن طريق الجمع بين حقول INDEX وSEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX والذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص الخاصة بحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// إذا كانت حقول XE تحتوي على نفس القيمة في خاصية "النص" الخاصة بها،
// سوف يقوم حقل INDEX بتجميعهم في إدخال واحد.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// في خاصية SequenceName، سمِّ تسلسل حقل SEQ. سيعرض الآن كل مُدخل في حقل INDEX هذا أيضًا
// الرقم الذي يقع عليه عدد التسلسل في موقع حقل XE الذي أنشأ هذا الإدخال.
index.SequenceName = "MySequence";

// تعيين النص الذي سيحيط بالتسلسل وأرقام الصفحات لشرح معناها للمستخدم.
// سيعرض الإدخال الذي تم إنشاؤه باستخدام هذا التكوين شيئًا مثل "MySequence في 1 على الصفحة 1" في رقم الصفحة الخاصة به.
// لا يمكن أن يتجاوز طول PageNumberSeparator وSequenceSeparator 15 حرفًا.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// تعرض حقول SEQ عددًا يتزايد عند كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بعدد منفصل لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" في حقل SEQ.
// أدخل حقل SEQ الذي يحرك تسلسل "MySequence" إلى 1.
// هذا الحقل لا يختلف عن نص المستند العادي. لن يظهر في جدول محتويات حقل الفهرس.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// أدخل حقل XE والذي سيقوم بإنشاء إدخال في حقل INDEX.
// نظرًا لأن "MySequence" موجود في 1 وحقل XE هذا موجود في الصفحة 2، إلى جانب الفواصل المخصصة التي حددناها أعلاه،
// سيعرض إدخال INDEX لهذا الحقل "Cat" على الجانب الأيسر، و"MySequence at 1 on page 2" على اليمين.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// أدخل فاصل الصفحة واستخدم حقول SEQ للتقدم "MySequence" إلى 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// قم بإدراج حقل XE بنفس خاصية النص الموجودة أعلاه.
// سيقوم إدخال INDEX بتجميع حقول XE مع القيم المطابقة في خاصية "النص"
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
// نظرًا لأننا في الصفحة 2 مع "MySequence" في 3، فسيتم إضافة ", 3 في الصفحة 3" إلى نفس إدخال INDEX كما هو مذكور أعلاه.
// سيعرض الآن جزء رقم الصفحة من إدخال INDEX "MySequence عند 1 في الصفحة 2، 3 في الصفحة 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// قم بإدراج حقل XE بقيمة خاصية نصية جديدة وفريدة.
// سيؤدي هذا إلى إضافة إدخال جديد، مع MySequence في رقم 3 على الصفحة 4.
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
