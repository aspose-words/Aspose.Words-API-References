---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: ParagraphFormat Bidi ملكية. الحصول على أو تحديد ما إذا كانت هذه فقرة من اليمين إلى اليسار في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

الحصول على أو تحديد ما إذا كانت هذه فقرة من اليمين إلى اليسار.

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

متى`حقيقي`، تم وضع عمليات التشغيل والكائنات المضمنة الأخرى في هذه الفقرة من اليمين إلى اليسار.

## أمثلة

يوضح كيفية اكتشاف اتجاه نص مستند النص العادي.

```csharp
// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// قم بتعيين خاصية "DocumentDirection" على "DocumentDirection.Auto" التي يتم اكتشافها تلقائيًا
// اتجاه كل فقرة من النص يقوم Aspose.Words بتحميلها من النص العادي.
// خاصية "Bidi" لكل فقرة ستخزن اتجاهها.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// كشف النص العبري من اليمين إلى اليسار.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// اكتشاف النص الإنجليزي باعتباره من اليمين إلى اليسار.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

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

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
