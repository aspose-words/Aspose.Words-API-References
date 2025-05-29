---
title: FieldSeq.ResetNumber
linktitle: ResetNumber
articleTitle: ResetNumber
second_title: Aspose.Words لـ .NET
description: أدر خاصية إعادة تعيين رقم FieldSeq بسهولة! عيّن أو استرجاع عدد صحيح للتحكم في أرقام التسلسل، مما يضمن معالجة دقيقة للبيانات.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldseq/resetnumber/
---
## FieldSeq.ResetNumber property

يحصل على أو يعيّن عددًا صحيحًا لإعادة تعيين الرقم التسلسلي إليه. يُرجع -1 إذا كان الرقم غير موجود.

```csharp
public string ResetNumber { get; set; }
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

### أنظر أيضا

* class [FieldSeq](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
