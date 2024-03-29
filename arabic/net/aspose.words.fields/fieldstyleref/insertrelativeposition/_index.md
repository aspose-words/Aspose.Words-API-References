---
title: FieldStyleRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words لـ .NET
description: FieldStyleRef InsertRelativePosition ملكية. الحصول على أو تعيين ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldstyleref/insertrelativeposition/
---
## FieldStyleRef.InsertRelativePosition property

الحصول على أو تعيين ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها.

```csharp
public bool InsertRelativePosition { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ قائمة بناءً على قالب قائمة Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// ستعرض هذه القائمة التي تم إنشاؤها "1.a )".
 // المسافة قبل القوس هي حرف غير محدد، ويمكننا حذفه.
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

// ضع حقل STYLEREF في الرأس واعرض أول نص بنمط "فقرة القائمة" في المستند.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// ضع حقل STYLEREF في التذييل، واجعله يعرض النص الأخير.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// يمكننا أيضًا استخدام حقول STYLEREF للإشارة إلى أرقام قوائم القوائم.
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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### أنظر أيضا

* class [FieldStyleRef](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
