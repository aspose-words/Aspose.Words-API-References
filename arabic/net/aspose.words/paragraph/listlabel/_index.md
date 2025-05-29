---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words لـ .NET
description: تمكّن من الوصول إلى ترقيم القوائم وتنسيقه باستخدام خاصية Paragraph ListLabel. حسّن تنظيم مستندك ووضوحه بسهولة!
type: docs
weight: 160
url: /ar/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

يحصل على`ListLabel`الكائن الذي يوفر الوصول إلى قيمة ترقيم القائمة وتنسيقها لهذه الفقرة.

```csharp
public ListLabel ListLabel { get; }
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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
