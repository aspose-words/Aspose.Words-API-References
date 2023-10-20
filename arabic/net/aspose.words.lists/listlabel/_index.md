---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Lists.ListLabel فصل. يحدد الخصائص الخاصة بتسمية القائمة في C#.
type: docs
weight: 3490
url: /ar/net/aspose.words.lists/listlabel/
---
## ListLabel class

يحدد الخصائص الخاصة بتسمية القائمة.

لمعرفة المزيد، قم بزيارة[العمل مع القوائم](https://docs.aspose.com/words/net/working-with-lists/) مقالة توثيقية.

```csharp
public class ListLabel
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | الحصول على خط تسمية القائمة. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | الحصول على تمثيل سلسلة لتسمية القائمة. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | الحصول على قيمة رقمية لهذه التسمية. |

## أمثلة

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

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
