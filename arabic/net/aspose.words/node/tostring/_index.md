---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words لـ .NET
description: Node ToString طريقة. تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد في C#.
type: docs
weight: 160
url: /ar/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد.

```csharp
public string ToString(SaveFormat saveFormat)
```

### قيمة الإرجاع

محتوى العقدة بالتنسيق المحدد.

## أمثلة

يُظهر الفرق بين استدعاء طريقتي GetText وToString على العقدة.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// سيقوم GetText باسترداد النص المرئي بالإضافة إلى رموز الحقول والأحرف الخاصة.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString سيعطينا مظهر المستند إذا تم حفظه بتنسيق حفظ تم تمريره.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

تصدير محتوى العقدة إلى String بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// عندما نستدعي طريقة ToString باستخدام التحميل الزائد لـ html SaveFormat،
// يقوم بتحويل محتويات العقدة إلى تمثيل HTML الخام الخاص بها.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

يوضح كيفية استخراج تسميات القائمة لجميع الفقرات التي تمثل عناصر قائمة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// اكتشف ما إذا كان لدينا قائمة الفقرات. في وثيقتنا، تستخدم قائمتنا أرقامًا عربية بسيطة،
// والتي تبدأ عند الثالثة وتنتهي عند السادسة.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // هذا هو النص الذي نحصل عليه عند إخراج هذه العقدة إلى تنسيق النص.
     // سيؤدي إخراج النص هذا إلى حذف تسميات القائمة. قم بقص أي أحرف بتنسيق الفقرة.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // يؤدي هذا إلى الحصول على موضع الفقرة في المستوى الحالي من القائمة. إذا كان لدينا قائمة ذات مستويات متعددة،
    // هذا سيخبرنا عن موقعه على هذا المستوى.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // اجمعها معًا لتضمين تسمية القائمة مع النص الموجود في الإخراج.
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

تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة.

```csharp
public string ToString(SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveOptions | SaveOptions | يحدد الخيارات التي تتحكم في كيفية حفظ العقدة. |

### قيمة الإرجاع

محتوى العقدة بالتنسيق المحدد.

## أمثلة

تصدير محتوى العقدة إلى String بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// عندما نستدعي طريقة ToString باستخدام التحميل الزائد لـ html SaveFormat،
// يقوم بتحويل محتويات العقدة إلى تمثيل HTML الخام الخاص بها.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
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
