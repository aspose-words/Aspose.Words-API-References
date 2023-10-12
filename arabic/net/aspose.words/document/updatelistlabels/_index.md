---
title: Document.UpdateListLabels
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. تحديث تسميات القائمة لجميع عناصر القائمة في المستند.
type: docs
weight: 780
url: /ar/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

تحديث تسميات القائمة لجميع عناصر القائمة في المستند.

```csharp
public void UpdateListLabels()
```

### ملاحظات

تقوم هذه الطريقة بتحديث خصائص تسمية القائمة مثل[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) و [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) لكل[`ListLabel`](../../paragraph/listlabel/)الكائن في المستند.

كما يتم أحيانًا استدعاء هذه الطريقة ضمنيًا عند تحديث الحقول في المستند. هذا مطلوب لأن بعض الحقول التي قد تشير إلى أرقام القائمة (مثل جدول المحتويات أو REF) تحتاج إلى تحديثها.

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


