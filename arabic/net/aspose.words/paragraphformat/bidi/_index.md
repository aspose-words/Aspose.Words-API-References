---
title: ParagraphFormat.Bidi
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تحديد ما إذا كانت هذه فقرة من اليمين إلى اليسار.
type: docs
weight: 40
url: /ar/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

الحصول على أو تحديد ما إذا كانت هذه فقرة من اليمين إلى اليسار.

```csharp
public bool Bidi { get; set; }
```

### ملاحظات

عندما يكون صحيحًا ، يتم تخطيط عمليات التشغيل والكائنات المضمنة الأخرى في هذه الفقرة من اليمين إلى اليسار.

### أمثلة

يوضح كيفية اكتشاف اتجاه نص مستند عادي.

```csharp
// قم بإنشاء كائن "TxtLoadOptions" ، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل كيفية تحميل مستند نص عادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// اضبط خاصية "DocumentDirection" على "DocumentDirection.Auto" بالكشف تلقائيًا
// اتجاه كل فقرة من النص يتم تحميل كلمات Aspose.Words من نص عادي.
// ستقوم خاصية "Bidi" الخاصة بكل فقرة بتخزين اتجاهها.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// كشف النص العبري من اليمين إلى اليسار.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// كشف النص الإنجليزي من اليمين إلى اليسار.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

يوضح كيفية إنشاء قوائم متوافقة مع اللغة ذات الاتجاه من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فقرات أرقام الحقول BIDIOUTLINE مثل حقول AUTONUM / LISTNUM ،
// ولكنه يكون مرئيًا فقط عند تمكين لغة تحرير من اليمين إلى اليسار ، مثل العبرية أو العربية.
// سيعرض الحقل التالي ".1" ، المكافئ RTL لرقم القائمة "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// أضف حقلين BIDIOUTLINE آخرين ، والذي سيعرض ".2" و ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// اضبط محاذاة النص الأفقي لكل فقرة في المستند على RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// إذا قمنا بتمكين لغة تحرير من اليمين إلى اليسار في Microsoft Word ، فستعرض الحقول الخاصة بنا الأرقام.
// وإلا فسيتم عرض "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


