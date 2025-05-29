---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: قم بمسح محتويات علامة المستند المنظم لديك بسهولة باستخدام طريقة المسح، وأظهر عنصر نائب محددًا لتحسين إدارة المستندات.
type: docs
weight: 360
url: /ar/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

يمسح محتويات علامة المستند المنظمة هذه ويعرض عنصرًا نائبًا إذا تم تعريفه.

```csharp
public void Clear()
```

## ملاحظات

ليس من الممكن مسح محتويات علامة المستند المنظم إذا كان يحتوي على مراجعات.

إذا تم تعيين علامة المستند المنظم هذه إلى XML مخصص (باستخدام[`XmlMapping`](../xmlmapping/)(خاصية )، يتم مسح عقدة XML المشار إليها.

## أمثلة

يوضح كيفية حذف محتويات عناصر علامة المستند المنظم.

```csharp
Document doc = new Document();

// قم بإنشاء علامة مستند نصية عادية، ثم قم بإضافتها إلى المستند.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// يعرض هذا المستند المنظم، والذي يكون على شكل مربع نص، نصًا نائبًا بالفعل.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// إنشاء كتلة بناء تحتوي على نص.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// قم بتعيين خاصية "PlaceholderName" الخاصة بعلامة المستند المنظم إلى اسم كتلة البناء الخاصة بنا للحصول على
// علامة المستند المنظم لعرض محتويات كتلة البناء بدلاً من النص الافتراضي الأصلي.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// قم بتحرير نص علامة المستند المنظم وإخفاء النص النائب.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// استخدم طريقة "مسح" لمسح محتويات علامة المستند المنظمة هذه وعرض العنصر النائب مرة أخرى.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
