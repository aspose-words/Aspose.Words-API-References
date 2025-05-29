---
title: Style.Aliases
linktitle: Aliases
articleTitle: Aliases
second_title: Aspose.Words لـ .NET
description: اكتشف جميع أسماء الأنماط البديلة بسهولة باستخدام خاصية "أسماء الأنماط البديلة". في حال عدم وجود أي منها، ستحصل على مصفوفة نصية فارغة. بسّط إدارة أنماطك!
type: docs
weight: 10
url: /ar/net/aspose.words/style/aliases/
---
## Style.Aliases property

يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أسماء مستعارة، فسيتم إرجاع مصفوفة فارغة من السلسلة.

```csharp
public string[] Aliases { get; }
```

## أمثلة

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
