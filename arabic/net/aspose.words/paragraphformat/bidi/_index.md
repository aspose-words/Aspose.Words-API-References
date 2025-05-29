---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat Bidi للتحكم بسهولة في تنسيق النص من اليمين إلى اليسار لتحسين قابلية القراءة وتحسين تخطيط المستند.
type: docs
weight: 50
url: /ar/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

يحصل على ما إذا كانت هذه الفقرة من اليمين إلى اليسار أو يحدد ما إذا كانت كذلك.

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

متى`حقيقي`، يتم عرض عمليات التشغيل والكائنات المضمنة الأخرى في هذه الفقرة من اليمين إلى اليسار.

## أمثلة

يوضح كيفية اكتشاف اتجاه نص المستند النصي العادي.

```csharp
// قم بإنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى منشئ المستند
// لتعديل كيفية تحميل مستند النص العادي.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// تعيين خاصية "DocumentDirection" إلى "DocumentDirection.Auto" يكتشف تلقائيًا
//اتجاه كل فقرة من النص الذي يقوم Aspose.Words بتحميله من النص العادي.
// ستقوم خاصية "Bidi" الخاصة بكل فقرة بتخزين اتجاهها.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// اكتشاف النص العبري من اليمين إلى اليسار.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// اكتشاف النص الإنجليزي من اليمين إلى اليسار.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

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

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
