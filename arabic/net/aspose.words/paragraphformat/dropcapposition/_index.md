---
title: ParagraphFormat.DropCapPosition
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تحديد موضع نص الأحرف الاستهلالية.
type: docs
weight: 90
url: /ar/net/aspose.words/paragraphformat/dropcapposition/
---
## ParagraphFormat.DropCapPosition property

الحصول على أو تحديد موضع نص الأحرف الاستهلالية.

```csharp
public DropCapPosition DropCapPosition { get; set; }
```

### أمثلة

يوضح كيفية دمج قائمة داخل قائمة أخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة الخطوط العريضة للعناوين.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// إنشاء قائمة ذات تعداد رقمي.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// كل فقرة تحتوي على قائمة سيكون لها هذا العلم.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// إنشاء قائمة نقطية.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// العودة إلى القائمة المرقمة.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// العودة إلى قائمة المخطط التفصيلي.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### أنظر أيضا

* enum [DropCapPosition](../../dropcapposition/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


