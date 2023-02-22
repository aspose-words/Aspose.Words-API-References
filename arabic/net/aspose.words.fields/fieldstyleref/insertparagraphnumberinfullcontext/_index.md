---
title: FieldStyleRef.InsertParagraphNumberInFullContext
second_title: Aspose.Words لمراجع .NET API
description: FieldStyleRef ملكية. الحصول على أو تحديد ما إذا كان سيتم إدراج رقم فقرة الفقرة المشار إليها في السياق الكامل.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/
---
## FieldStyleRef.InsertParagraphNumberInFullContext property

الحصول على أو تحديد ما إذا كان سيتم إدراج رقم فقرة الفقرة المشار إليها في السياق الكامل.

```csharp
public bool InsertParagraphNumberInFullContext { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقول STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء قائمة باستخدام قالب قائمة Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// ستعرض هذه القائمة التي تم إنشاؤها "1.a)".
 // المسافة قبل القوس هي حرف غير محدد ، يمكننا منعه.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// أضف نصًا وقم بتطبيق أنماط الفقرة التي ستشير إليها حقول STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// ضع حقل STYLEREF في الرأس واعرض أول نص على غرار "قائمة فقرة" في المستند.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// ضع حقل STYLEREF في التذييل ، واجعله يعرض آخر نص.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// يمكننا أيضًا استخدام حقول STYLEREF للإشارة إلى أرقام قائمة القوائم.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### أنظر أيضا

* class [FieldStyleRef](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldstyleref/)
* المجسم [Aspose.Words](../../../)


