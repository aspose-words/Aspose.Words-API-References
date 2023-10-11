---
title: ListLabel.LabelValue
second_title: Aspose.Words لمراجع .NET API
description: ListLabel ملكية. الحصول على قيمة رقمية لهذه التسمية.
type: docs
weight: 30
url: /ar/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

الحصول على قيمة رقمية لهذه التسمية.

```csharp
public int LabelValue { get; }
```

### ملاحظات

استخدم[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) طريقة لتحديث قيمة هذه الخاصية.

### أمثلة

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

* class [ListLabel](../)
* مساحة الاسم [Aspose.Words.Lists](../../listlabel/)
* المجسم [Aspose.Words](../../../)


