---
title: IStructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية العنصر النائب IStructuredDocumentTag. أدر بسهولة النص النائب لمحتوى SDT الفارغ، وحسّن استخدام مستندك.
type: docs
weight: 100
url: /ar/net/aspose.words.markup/istructureddocumenttag/placeholder/
---
## IStructuredDocumentTag.Placeholder property

يحصل على[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب يجب عرضه عندما تكون محتويات تشغيل SDT هذه فارغة، عنصر XML المرتبط فارغًا كما هو محدد عبر[`XmlMapping`](../xmlmapping/) element أو[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) العنصر صحيح.

```csharp
public BuildingBlock Placeholder { get; }
```

## ملاحظات

يمكن أن يكون فارغًا، مما يعني أن العنصر النائب غير قابل للتطبيق على هذا Sdt.

## أمثلة

يوضح كيفية استخدام محتويات كتلة البناء كنص مخصص لعلامة مستند منظمة.

```csharp
Document doc = new Document();

// قم بإدراج علامة مستند منظمة نصية عادية من نوع "PlainText"، والتي ستعمل كمربع نص.
// المحتوى الذي سيتم عرضه بشكل افتراضي هو عبارة عن مطالبة "انقر هنا لإدخال النص".
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// يمكننا جعل العلامة تعرض محتويات كتلة البناء بدلاً من النص الافتراضي.
// أولاً، أضف كتلة بناء تحتوي على محتويات إلى مستند المصطلحات.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// ثم استخدم خاصية "PlaceholderName" الموجودة في علامة المستند المنظم للإشارة إلى كتلة البناء هذه بالاسم.
tag.PlaceholderName = "Custom Placeholder";

// إذا كان "PlaceholderName" يشير إلى كتلة موجودة في مستند المصطلحات الخاص بالمستند الرئيسي،
// سوف نكون قادرين على التحقق من كتلة البناء من خلال خاصية "Placeholder".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// اضبط خاصية "IsShowingPlaceholderText" على "true" لمعالجة
// المحتويات الحالية لعلامة المستند المنظم كنص بديل.
// وهذا يعني أن النقر فوق مربع النص في Microsoft Word سيؤدي على الفور إلى تسليط الضوء على كافة محتويات العلامة.
// اضبط خاصية "IsShowingPlaceholderText" على "false" للحصول على
// علامة مستند منظمة لمعاملة محتوياتها كنص أدخله المستخدم بالفعل.
// النقر فوق هذا النص في Microsoft Word سيضع المؤشر الوامض في الموقع الذي تم النقر فوقه.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### أنظر أيضا

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
