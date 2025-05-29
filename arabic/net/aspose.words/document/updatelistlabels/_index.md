---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words لـ .NET
description: قم بتحديث جميع تسميات عناصر القائمة في مستندك بسهولة باستخدام طريقة UpdateListLabels، مما يضمن الاتساق والوضوح في المحتوى الخاص بك.
type: docs
weight: 820
url: /ar/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

تحديث تسميات القائمة لجميع عناصر القائمة في المستند.

```csharp
public void UpdateListLabels()
```

## ملاحظات

تقوم هذه الطريقة بتحديث خصائص تسمية القائمة مثل[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) و [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) لكل واحد[`ListLabel`](../../paragraph/listlabel/) الكائن في المستند.

أيضًا، يتم أحيانًا استدعاء هذه الطريقة ضمنيًا عند تحديث حقول المستند. هذه الطريقة مطلوبة لأن بعض الحقول التي قد تشير إلى أرقام قوائم (مثل جدول المحتويات أو المرجع) تحتاج إلى تحديثها.

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
