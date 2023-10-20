---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words لـ .NET
description: Style BaseStyleName ملكية. الحصول على/تعيين اسم النمط الذي يعتمد عليه هذا النمط في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

الحصول على/تعيين اسم النمط الذي يعتمد عليه هذا النمط.

```csharp
public string BaseStyleName { get; set; }
```

## ملاحظات

ستكون هذه سلسلة فارغة إذا كان النمط لا يعتمد على أي نمط آخر ويمكن ضبطه على سلسلة فارغة.

## أمثلة

يوضح كيفية استخدام الأسماء المستعارة للأسلوب.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// يحتوي هذا المستند على نمط يسمى "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// إذا كان اسم النمط يحتوي على قيم متعددة مفصولة بفواصل، فستكون كل جملة اسمًا مستعارًا منفصلاً.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// يمكننا الإشارة إلى النمط باستخدام اسمه المستعار، بالإضافة إلى اسمه.
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
