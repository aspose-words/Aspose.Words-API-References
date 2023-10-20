---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag Clear طريقة. يمسح محتويات علامة المستند المنظمة ويعرض عنصرًا نائبًا إذا تم تعريفه في C#.
type: docs
weight: 340
url: /ar/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

يمسح محتويات علامة المستند المنظمة ويعرض عنصرًا نائبًا إذا تم تعريفه.

```csharp
public void Clear()
```

## ملاحظات

ليس من الممكن مسح محتويات علامة المستند المنظمة إذا كانت تحتوي على مراجعات.

إذا تم تعيين علامة المستند المنظمة هذه إلى XML مخصص (باستخدام[`XmlMapping`](../xmlmapping/) )، يتم مسح عقدة XML المشار إليها.

## أمثلة

يوضح كيفية حذف محتويات عناصر علامة المستند المنظمة.

```csharp
Document doc = new Document();

// أنشئ علامة مستند منظمة بنص عادي، ثم ألحقها بالمستند.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// علامة المستند المنظمة هذه، والتي تكون على شكل مربع نص، تعرض بالفعل نص العنصر النائب.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// قم بإنشاء كتلة بناء بمحتويات النص.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// قم بتعيين خاصية "PlaceholderName" الخاصة بعلامة المستند المنظمة على اسم الكتلة البرمجية الخاصة بنا للحصول عليها
// علامة المستند المنظمة لعرض محتويات الكتلة البرمجية الإنشائية بدلاً من النص الافتراضي الأصلي.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// قم بتحرير نص علامة المستند المنظمة وإخفاء نص العنصر النائب.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// استخدم الطريقة "مسح" لمسح محتويات علامة المستند المنظمة هذه وعرض العنصر النائب مرة أخرى.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
