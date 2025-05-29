---
title: ParagraphFormat.DropCapPosition
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat DropCapPosition لتخصيص موضع نص الحرف الكبير بسهولة لتحسين تصميم المستند وسهولة قراءته.
type: docs
weight: 100
url: /ar/net/aspose.words/paragraphformat/dropcapposition/
---
## ParagraphFormat.DropCapPosition property

يحصل على موضع النص ذي الأحرف الكبيرة أو يعينه.

```csharp
public DropCapPosition DropCapPosition { get; set; }
```

## أمثلة

يوضح كيفية تعشيش قائمة داخل قائمة أخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة مخططة للعناوين.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// إنشاء قائمة مرقمة.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// كل فقرة تتكون من قائمة سيكون لها هذا العلم.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// إنشاء قائمة نقطية.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

//العودة إلى القائمة المرقمة.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

//العودة إلى قائمة المخطط التفصيلي.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### أنظر أيضا

* enum [DropCapPosition](../../dropcapposition/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
