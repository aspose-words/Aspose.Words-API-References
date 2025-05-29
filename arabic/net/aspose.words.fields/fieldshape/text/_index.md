---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: يمكنك إدارة نص FieldShape بسهولة - احصل على القيم أو قم بتعيينها دون عناء لاسترجاع البيانات بسلاسة وتحسين الوظائف في تطبيقاتك.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

يحصل على النص الذي سيتم استرداده أو يعينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية إنشاء قوائم متوافقة مع اللغة من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يقوم حقل BIDIOUTLINE بترقيم الفقرات مثل حقول AUTONUM/LISTNUM،
// ولكن لا يمكن رؤيته إلا عند تمكين لغة التحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
// سيعرض الحقل التالي ".1"، وهو المعادل من RTL لرقم القائمة "1".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// أضف حقلين آخرين من BIDIOUTLINE، والذي سيعرض ".2" و".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// قم بتعيين محاذاة النص الأفقية لكل فقرة في المستند إلى RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// إذا قمنا بتمكين لغة التحرير من اليمين إلى اليسار في Microsoft Word، فستعرض حقولنا أرقامًا.
// وإلا، فسوف يتم عرض "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

يوضح كيفية التعامل مع بعض حقول Microsoft Word القديمة مثل SHAPE وEMBED أثناء التحميل.

```csharp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// إذا فتحنا مستند Word وضغطنا على Alt+F9، فسنرى حقل SHAPE وحقل EMBED.
// حقل الشكل هو المرساة/اللوحة القماشية لكائن الشكل التلقائي مع تمكين نمط الالتفاف "متوافق مع النص".
// حقل EMBED له نفس الوظيفة، ولكن بالنسبة للكائن المضمن،
// مثل جدول بيانات من مستند Excel خارجي.
// ومع ذلك، لن تظهر هذه الحقول في مجموعة الحقول الخاصة بالمستند.
Assert.AreEqual(0, doc.Range.Fields.Count);

// هذه الحقول مدعومة فقط بواسطة الإصدارات القديمة من Microsoft Word.
// ستعمل عملية تحميل المستند على تحويل هذه الحقول إلى كائنات شكلية،
// والتي يمكننا الوصول إليها في مجموعة عقد المستند.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// تتوافق عقدة الشكل الأولى مع حقل الشكل في المستند المدخل،
// وهو القماش المضمن للشكل التلقائي.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// عقدة الشكل الثانية هي الشكل التلقائي نفسه.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// الشكل الثالث هو الحقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### أنظر أيضا

* class [FieldShape](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
