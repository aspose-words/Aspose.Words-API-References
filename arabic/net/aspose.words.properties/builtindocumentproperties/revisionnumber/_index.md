---
title: BuiltInDocumentProperties.RevisionNumber
linktitle: RevisionNumber
articleTitle: RevisionNumber
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties RevisionNumber ملكية. الحصول على رقم مراجعة المستند أو تعيينه في C#.
type: docs
weight: 240
url: /ar/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

الحصول على رقم مراجعة المستند أو تعيينه.

```csharp
public int RevisionNumber { get; set; }
```

## ملاحظات

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

يوضح كيفية العمل مع حقول REVNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// أدخل حقل REVNUM، الذي يعرض خاصية رقم المراجعة الحالية للمستند.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// تحسب هذه الخاصية عدد مرات حفظ المستند في برنامج Microsoft Word،
// ولا علاقة له بالمراجعات المتعقبة. يمكننا العثور عليه عن طريق النقر بزر الماوس الأيمن على المستند في مستكشف Windows
// عبر الخصائص -> تفاصيل. يمكننا تحديث هذه الخاصية يدويًا.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

يوضح كيفية العمل مع خصائص المستند في فئة "الأصل".

```csharp
// افتح مستندًا قمنا بإنشائه وتحريره باستخدام Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// تحتوي الخصائص المضمنة التالية على معلومات تتعلق بإنشاء هذا المستند وتحريره.
// يمكننا النقر بزر الماوس الأيمن فوق هذا المستند في مستكشف Windows والعثور عليه
// هذه الخصائص عبر "الخصائص" -> "التفاصيل" -> فئة "الأصل".
// يمكن لحقول مثل PRINTDATE وEDITTIME عرض هذه القيم في نص المستند.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// يمكننا أيضًا تغيير قيم الخصائص المضمنة.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// يقوم Microsoft Word بتحديث الخصائص التالية تلقائيًا عندما نحفظ المستند.
// لاستخدام هذه الخصائص مع Aspose.Words، سنحتاج إلى تعيين قيم لها يدويًا.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// يمكننا النقر بزر الماوس الأيمن فوق هذا المستند في مستكشف Windows والعثور عليه these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
