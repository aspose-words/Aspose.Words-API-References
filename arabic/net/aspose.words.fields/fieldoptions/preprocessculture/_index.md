---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل FieldOptions PreProcessCulture على تعزيز معالجة البيانات الخاصة بك عن طريق تخصيص ثقافات قيمة الحقل لتحسين الدقة والكفاءة.
type: docs
weight: 170
url: /ar/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

يحصل على الثقافة أو يعينها لمعالجة قيم الحقول مسبقًا.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## ملاحظات

حاليًا، تؤثر هذه الخاصية فقط على قيمة[`FieldDocProperty`](../../fielddocproperty/) مجال.

القيمة الافتراضية هي`باطل` . عندما يتم تعيين هذه الخاصية على`باطل` ، ال[`FieldDocProperty`](../../fielddocproperty/) قيمة الحقل هي preprocessed مع الثقافة التي يتم التحكم فيها بواسطة[`FieldUpdateCultureSource`](../fieldupdateculturesource/) ملكية.

## أمثلة

يوضح كيفية ضبط ثقافة المعالجة المسبقة.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين الثقافة التي سيتم بموجبها تنسيق بعض الحقول للقيم المعروضة.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// سيعرض حقل DOCPROPERTY نتيجته بتنسيق وفقًا لثقافة المعالجة المسبقة
// لقد ضبطنا الإعدادات على الألمانية. سيعرض الحقل التاريخ/الوقت بتنسيق "dd.mm.yyyy hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// بعد التبديل إلى الثقافة الثابتة، سيستخدم حقل DOCPROPERTY تنسيق "mm/dd/yyyy hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
