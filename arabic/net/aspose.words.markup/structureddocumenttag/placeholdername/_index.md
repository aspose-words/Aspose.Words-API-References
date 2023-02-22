---
title: StructuredDocumentTag.PlaceholderName
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحصل أو يحدد اسمBuildingBlock تحتوي على نص عنصر نائب.
type: docs
weight: 240
url: /ar/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

يحصل أو يحدد اسم[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) تحتوي على نص عنصر نائب.

BuildingBlock بهذا الاسم[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) يجب أن يكون موجودًا في[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) خلاف ذلكInvalidOperationException سوف يحدث.

```csharp
public string PlaceholderName { get; set; }
```

### أمثلة

يوضح كيفية استخدام محتويات الكتلة البرمجية الإنشائية كنص عنصر نائب مخصص لعلامة مستند منظم.

```csharp
Document doc = new Document();

// أدخل علامة مستند منظم بنص عادي من نوع "نص عادي" ، والذي سيعمل كمربع نص.
// المحتويات التي سيتم عرضها افتراضيًا هي "انقر هنا لإدخال نص." مستعجل.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// يمكننا الحصول على العلامة لعرض محتويات الكتلة البرمجية الإنشائية بدلاً من النص الافتراضي.
// أولاً ، أضف عنصر إنشاء بمحتويات إلى مستند المسرد.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// ثم استخدم خاصية "PlaceholderName" لعلامة المستند المهيكلة للإشارة إلى كتلة الإنشاء هذه بالاسم.
tag.PlaceholderName = "Custom Placeholder";

// إذا كان "PlaceholderName" يشير إلى كتلة موجودة في مستند قاموس مصطلحات المستند الأصلي ،
// سنتمكن من التحقق من الكتلة البرمجية الإنشائية عبر خاصية "Placeholder".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// اضبط خاصية "IsShowingPlaceholderText" على "true" لمعالجة ملف
// محتويات علامة المستند المهيكلة الحالية كنص عنصر نائب.
// هذا يعني أن النقر فوق مربع النص في Microsoft Word سيبرز على الفور جميع محتويات العلامة.
// اضبط خاصية "IsShowingPlaceholderText" على "false" للحصول على ملف
// علامة مستند منظم للتعامل مع محتوياته كنص أدخله المستخدم بالفعل.
// سيؤدي النقر فوق هذا النص في Microsoft Word إلى وضع المؤشر الوامض في الموقع الذي تم النقر عليه.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


