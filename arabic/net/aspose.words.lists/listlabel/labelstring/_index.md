---
title: ListLabel.LabelString
linktitle: LabelString
articleTitle: LabelString
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListLabel LabelString لتمثيل سلسلة تسميات القائمة بسهولة، مما يعزز عرض بياناتك وتنظيمها بسهولة.
type: docs
weight: 20
url: /ar/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

يحصل على تمثيل سلسلة لعلامة القائمة.

```csharp
public string LabelString { get; }
```

## أمثلة

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

* class [ListLabel](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
