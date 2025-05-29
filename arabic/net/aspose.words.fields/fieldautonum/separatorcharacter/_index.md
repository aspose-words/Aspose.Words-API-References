---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldAutoNum SeparatorCharacter، وقم بتخصيص حرف الفاصل الخاص بك بسهولة لتحسين تنسيق البيانات وتحسين إمكانية الاستخدام.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

يحصل على حرف الفاصل الذي سيتم استخدامه أو يعينه.

```csharp
public string SeparatorCharacter { get; set; }
```

## أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول الترقيم التلقائي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يعرض كل حقل AUTONUM القيمة الحالية لعدد تشغيلي لحقول AUTONUM،
// مما يسمح لنا بترقيم العناصر تلقائيًا مثل القائمة المرقمة.
//سيعرض هذا الحقل الرقم "1".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// حرف الفاصل، الذي يظهر في نتيجة الحقل مباشرة بعد الرقم، هو نقطة افتراضيًا.
// إذا تركنا هذه الخاصية فارغة، فسوف يعرض حقل AUTONUM الثاني الرقم "2." في المستند.
Assert.IsNull(field.SeparatorCharacter);

// يمكننا تعيين هذه الخاصية لتطبيق الحرف الأول من السلسلة كحرف فاصل جديد.
// في هذه الحالة، سيعرض حقل AUTONUM الخاص بنا الآن "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### أنظر أيضا

* class [FieldAutoNum](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
