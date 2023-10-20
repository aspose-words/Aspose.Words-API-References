---
title: StructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag PlaceholderName ملكية. الحصول على أو تعيين اسمBuildingBlock تحتوي على نص نائب في C#.
type: docs
weight: 240
url: /ar/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

الحصول على أو تعيين اسم[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) تحتوي على نص نائب.

[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) بهذا الاسم[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) يجب أن يكون موجودا في[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) خلاف ذلكInvalidOperationException سوف يحدث.

```csharp
public string PlaceholderName { get; set; }
```

## أمثلة

يوضح كيفية استخدام محتويات الكتلة البرمجية الإنشائية كنص عنصر نائب مخصص لعلامة مستند منظمة.

```csharp
Document doc = new Document();

// قم بإدراج علامة مستند منظمة لنص عادي من النوع "PlainText"، والتي ستعمل كمربع نص.
// المحتويات التي سيتم عرضها بشكل افتراضي هي "انقر هنا لإدخال النص." اِسْتَدْعَى.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// يمكننا جعل العلامة تعرض محتويات الكتلة البرمجية الإنشائية بدلاً من النص الافتراضي.
// أولاً، أضف كتلة إنشاء تحتوي على محتويات إلى مستند المسرد.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// بعد ذلك، استخدم خاصية "PlaceholderName" الخاصة بعلامة المستند المنظم للإشارة إلى الكتلة البرمجية الإنشائية تلك بالاسم.
tag.PlaceholderName = "Custom Placeholder";

// إذا كان "PlaceholderName" يشير إلى كتلة موجودة في مستند المصطلحات الخاص بالمستند الأصلي،
// سنكون قادرين على التحقق من الكتلة البرمجية الإنشائية عبر خاصية "العنصر النائب".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// قم بتعيين خاصية "IsShowingPlaceholderText" على "صحيح" للتعامل مع
// المحتويات الحالية لعلامة المستند المنظمة كنص نائب.
// هذا يعني أن النقر فوق مربع النص في Microsoft Word سيؤدي فورًا إلى تمييز جميع محتويات العلامة.
// قم بتعيين خاصية "IsShowingPlaceholderText" على "خطأ" للحصول على القيمة "خطأ".
// علامة مستند منظمة للتعامل مع محتوياتها كنص أدخله المستخدم بالفعل.
// سيؤدي النقر فوق هذا النص في Microsoft Word إلى وضع المؤشر الوامض في الموقع الذي تم النقر عليه.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
