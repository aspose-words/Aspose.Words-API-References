---
title: StructuredDocumentTag.Placeholder
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. يحصل علىBuildingBlockيحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل SDT فارغة عنصر XML المعين المرتبط فارغ كما هو محدد عبرXmlMapping element أوIsShowingPlaceholderText العنصر هوحقيقي .
type: docs
weight: 230
url: /ar/net/aspose.words.markup/structureddocumenttag/placeholder/
---
## StructuredDocumentTag.Placeholder property

يحصل على[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)يحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل SDT فارغة، عنصر XML المعين المرتبط فارغ كما هو محدد عبر[`XmlMapping`](../xmlmapping/) element أو[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) العنصر هو`حقيقي` .

```csharp
public BuildingBlock Placeholder { get; }
```

### ملاحظات

يمكن ان يكون`باطل`، وهذا يعني أن العنصر النائب لا ينطبق على هذه المعاملة الخاصة والتفضيلية.

### أمثلة

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

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


