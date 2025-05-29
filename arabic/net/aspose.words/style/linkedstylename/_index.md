---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تصميم خاصية LinkedStyleName وإدارة الأنماط المرتبطة بسهولة وتعزيز سير عمل التصميم الخاص بك من خلال التكامل السلس.
type: docs
weight: 90
url: /ar/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

يحصل على/يحدد اسم[`Style`](../) مرتبط بهذا. يُرجع سلسلة فارغة إذا لم تكن هناك أنماط مرتبطة.

```csharp
public string LinkedStyleName { get; set; }
```

## ملاحظات

لا يجوز إلا ربط نمط الفقرة بنمط الحرف والعكس.

يؤدي تعيين LinkedStyleName للنمط الحالي تلقائيًا إلى تعيين LinkedStyleName للنمط المرتبط.

إن تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط سابقًا.

## أمثلة

يوضح كيفية ربط الأنماط مع بعضها البعض.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

يوضح كيفية استخدام أسماء الأنماط البديلة.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// تحتوي هذه الوثيقة على نمط يسمى "MyStyle،MyStyle Alias 1،MyStyle Alias 2".
// إذا كان اسم النمط يحتوي على قيم متعددة مفصولة بفاصلات، فإن كل جملة هي اسم مستعار منفصل.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

//يمكننا الإشارة إلى نمط ما باستخدام اسمه المستعار، بالإضافة إلى اسمه.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
