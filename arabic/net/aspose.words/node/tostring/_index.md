---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Node ToString، وحوّل محتوى العقدة إلى سلاسل نصية بسهولة تامة بتنسيقات قابلة للتخصيص لتحسين معالجة البيانات. حسّن برمجة جهازك اليوم!
type: docs
weight: 160
url: /ar/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد.

```csharp
public string ToString(SaveFormat saveFormat)
```

### قيمة الإرجاع

محتوى العقدة بالتنسيق المحدد.

## أمثلة

يُظهر الفرق بين استدعاء طريقتي GetText وToString على عقدة.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// سيقوم GetText باسترجاع النص المرئي بالإضافة إلى رموز الحقول والأحرف الخاصة.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// سيعطينا ToString مظهر المستند إذا تم حفظه بتنسيق الحفظ الذي تم تمريره.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

يقوم بتصدير محتوى العقدة إلى سلسلة بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// عندما نستدعي طريقة ToString باستخدام التحميل الزائد لـ SaveFormat في html،
// يقوم بتحويل محتويات العقدة إلى تمثيلها الخام بصيغة HTML.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

//يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

يوضح كيفية استخراج تسميات القائمة لجميع الفقرات التي تعد عناصر قائمة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// ابحث إن كانت لدينا قائمة الفقرات. في مستندنا، تستخدم قائمتنا أرقامًا عربية بسيطة،
// والتي تبدأ عند ثلاثة وتنتهي عند ستة.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // هذا هو النص الذي نحصل عليه عندما نخرج هذه العقدة إلى تنسيق نصي.
     // سيحذف هذا النص تسميات القائمة. قم بقص أي أحرف تنسيق للفقرات.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // يُحدد هذا موضع الفقرة في المستوى الحالي من القائمة. إذا كانت لدينا قائمة ذات مستويات متعددة،
    // هذا سيخبرنا ما هو الموضع على هذا المستوى.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // قم بدمجهما معًا لتضمين تسمية القائمة مع النص في الإخراج.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### أنظر أيضا

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة.

```csharp
public string ToString(SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ العقدة. |

### قيمة الإرجاع

محتوى العقدة بالتنسيق المحدد.

## أمثلة

يقوم بتصدير محتوى العقدة إلى سلسلة بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// عندما نستدعي طريقة ToString باستخدام التحميل الزائد لـ SaveFormat في html،
// يقوم بتحويل محتويات العقدة إلى تمثيلها الخام بصيغة HTML.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

//يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
