---
title: FieldAutoNum.SeparatorCharacter
second_title: Aspose.Words لمراجع .NET API
description: FieldAutoNum ملكية. الحصول على أو تعيين الحرف الفاصل الذي سيتم استخدامه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

الحصول على أو تعيين الحرف الفاصل الذي سيتم استخدامه.

```csharp
public string SeparatorCharacter { get; set; }
```

### أمثلة

يوضح كيفية ترقيم الفقرات باستخدام حقول التجميع التلقائي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يعرض كل حقل AUTONUM القيمة الحالية لعدد التشغيل لحقول AUTONUM ،
// مما يسمح لنا بترقيم العناصر تلقائيًا مثل قائمة مرقمة.
// سيعرض هذا الحقل الرقم "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// الحرف الفاصل ، الذي يظهر في نتيجة الحقل مباشرة بعد الرقم ، هو نقطة توقف بشكل افتراضي.
// إذا تركنا هذه الخاصية فارغة ، فسيعرض حقل AUTONUM الثاني "2." في المستند.
Assert.IsNull(field.SeparatorCharacter);

// يمكننا تعيين هذه الخاصية لتطبيق الحرف الأول من سلسلتها كحرف فاصل جديد.
// في هذه الحالة ، سيعرض حقل AUTONUM الآن "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### أنظر أيضا

* class [FieldAutoNum](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldautonum/)
* المجسم [Aspose.Words](../../../)


