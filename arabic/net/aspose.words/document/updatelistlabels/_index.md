---
title: Document.UpdateListLabels
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. تحديث تسميات القائمة لكافة عناصر القائمة في المستند.
type: docs
weight: 740
url: /ar/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

تحديث تسميات القائمة لكافة عناصر القائمة في المستند.

```csharp
public void UpdateListLabels()
```

### ملاحظات

تقوم هذه الطريقة بتحديث خصائص تسمية القائمة مثل[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) و_ [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/)لكل[`ListLabel`](../../paragraph/listlabel/) كائن في المستند.

أيضًا ، يتم أحيانًا استدعاء هذه الطريقة ضمنيًا عند تحديث الحقول في المستند. هذا required لأن بعض الحقول التي قد تشير إلى أرقام القائمة (مثل TOC أو REF) تحتاج إلى أن تكون محدثة.

### أمثلة

يوضح كيفية استخراج تسميات القائمة لكل الفقرات التي تمثل عناصر قائمة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// ابحث عما إذا كان لدينا قائمة الفقرات. في وثيقتنا ، تستخدم قائمتنا أرقامًا عربية بسيطة ،
// التي تبدأ عند الثالثة وتنتهي عند السادسة.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // هذا هو النص الذي نحصل عليه عند إخراج هذه العقدة إلى تنسيق نصي.
    // سيحذف إخراج النص هذا تسميات القائمة. تقليم أي أحرف تنسيق الفقرة. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // هذا يحصل على موضع الفقرة في المستوى الحالي من القائمة. إذا كانت لدينا قائمة بمستويات متعددة ،
    // سيخبرنا هذا بالموقع الذي وصلت إليه على هذا المستوى.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // اجمعها معًا لتضمين تسمية القائمة مع النص في الإخراج.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


