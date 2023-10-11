---
title: FieldShape.Text
second_title: Aspose.Words لمراجع .NET API
description: FieldShape ملكية. الحصول على النص أو تعيينه لاسترداده.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

الحصول على النص أو تعيينه لاسترداده.

```csharp
public string Text { get; set; }
```

### أمثلة

يوضح كيفية إنشاء قوائم متوافقة مع اللغة من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يقوم حقل BIDIOUTLINE بترقيم الفقرات مثل حقول AUTONUM/LISTNUM،
// ولكنه يكون مرئيًا فقط عند تمكين لغة التحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
// سيعرض الحقل التالي ".1"، وهو ما يعادل رقم القائمة "1." من اليمين إلى اليسار (RTL).
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// أضف حقلين آخرين لـ BIDIOUTLINE، حيث سيتم عرض ".2" و".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// اضبط محاذاة النص الأفقي لكل فقرة في المستند على RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// إذا قمنا بتمكين لغة التحرير من اليمين إلى اليسار في Microsoft Word، فستعرض حقولنا أرقامًا.
// وإلا فسوف يعرضون "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

يوضح كيفية التعامل مع بعض حقول Microsoft Word القديمة مثل SHAPE وEMBED أثناء التحميل.

```csharp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// إذا فتحنا مستند Word واضغطنا على Alt+F9، فسنرى شكلًا وحقل EMBED.
// حقل SHAPE هو نقطة الارتساء/اللوحة القماشية لكائن الشكل التلقائي مع تمكين نمط الالتفاف "سطري مع النص".
// حقل EMBED له نفس الوظيفة، ولكن بالنسبة للكائن المضمن،
// مثل جدول بيانات من مستند Excel خارجي.
// ومع ذلك، لن تظهر هذه الحقول في مجموعة حقول المستند.
Assert.AreEqual(0, doc.Range.Fields.Count);

// هذه الحقول مدعومة فقط في الإصدارات القديمة من Microsoft Word.
// ستقوم عملية تحميل المستند بتحويل هذه الحقول إلى كائنات الشكل،
// والتي يمكننا الوصول إليها في مجموعة عقدة المستند.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// تتوافق عقدة الشكل الأولى مع حقل SHAPE في مستند الإدخال،
// وهي اللوحة المضمنة للشكل التلقائي.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// عقدة الشكل الثانية هي الشكل التلقائي نفسه.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// الشكل الثالث هو حقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### أنظر أيضا

* class [FieldShape](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldshape/)
* المجسم [Aspose.Words](../../../)


