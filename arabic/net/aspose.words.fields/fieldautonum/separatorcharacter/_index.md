---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words لـ .NET
description: FieldAutoNum SeparatorCharacter ملكية. الحصول على أو تعيين الحرف الفاصل المطلوب استخدامه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

الحصول على أو تعيين الحرف الفاصل المطلوب استخدامه.

```csharp
public string SeparatorCharacter { get; set; }
```

## أمثلة

يوضح كيفية ترقيم الفقرات باستخدام الحقول التلقائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يعرض كل حقل AUTONUM القيمة الحالية للعدد الجاري لحقول AUTONUM،
// السماح لنا بترقيم العناصر تلقائيًا مثل قائمة مرقمة.
// سيعرض هذا الحقل الرقم "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// الحرف الفاصل، الذي يظهر في نتيجة الحقل مباشرة بعد الرقم، هو نقطة بشكل افتراضي.
// إذا تركنا هذه الخاصية فارغة، فسيعرض الحقل التلقائي الثاني لدينا "2." في الوثيقة.
Assert.IsNull(field.SeparatorCharacter);

// يمكننا ضبط هذه الخاصية لتطبيق الحرف الأول من السلسلة الخاصة بها كحرف فاصل جديد.
// في هذه الحالة، سيعرض حقل AUTONUM الخاص بنا الآن "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### أنظر أيضا

* class [FieldAutoNum](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
