---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Lists.ListLabel لتحسين تنسيق مستندك باستخدام خصائص تسمية القائمة القابلة للتخصيص لتحسين التحكم والعرض.
type: docs
weight: 3940
url: /ar/net/aspose.words.lists/listlabel/
---
## ListLabel class

يحدد خصائص محددة بتسمية القائمة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListLabel
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | يحصل على خط تسمية القائمة. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | يحصل على تمثيل سلسلة لعلامة القائمة. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | يحصل على قيمة عددية لهذه العلامة. |

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

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
