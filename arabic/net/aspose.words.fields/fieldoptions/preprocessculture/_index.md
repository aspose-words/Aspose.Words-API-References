---
title: FieldOptions.PreProcessCulture
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على الثقافة أو تعيينها لمعالجة قيم الحقول مسبقًا.
type: docs
weight: 170
url: /ar/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

الحصول على الثقافة أو تعيينها لمعالجة قيم الحقول مسبقًا.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### ملاحظات

حاليا هذه الخاصية تؤثر فقط على قيمة[`FieldDocProperty`](../../fielddocproperty/) مجال.

القيمة الافتراضية هي`باطل` . عندما يتم تعيين هذه الخاصية إلى`باطل` ، ال[`FieldDocProperty`](../../fielddocproperty/)تتم معالجة قيمة الحقل مسبقًا مع الثقافة التي يتحكم فيها[`FieldUpdateCultureSource`](../fieldupdateculturesource/) ملكية.

### أمثلة

يوضح كيفية ضبط ثقافة المعالجة المسبقة.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين الثقافة التي ستقوم بعض الحقول وفقًا لها بتنسيق قيمها المعروضة.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// سيعرض حقل DOCPROPERTY النتيجة المنسقة وفقًا لثقافة المعالجة المسبقة
// لقد وضعنا على اللغة الألمانية. سيعرض الحقل التاريخ/الوقت باستخدام التنسيق "dd.mm.yyyy hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// بعد التبديل إلى الثقافة الثابتة، سيستخدم حقل DOCPROPERTY التنسيق "mm/dd/yyyy hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


