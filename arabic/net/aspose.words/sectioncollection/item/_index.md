---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى أقسام محددة بسهولة باستخدام خاصية SectionCollection Item. استرجع أي قسم حسب الفهرس لإدارة بيانات مبسطة.
type: docs
weight: 10
url: /ar/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

يسترجع قسمًا في الفهرس المحدد.

```csharp
public Section this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس لقائمة الأقسام. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

## أمثلة

يُظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيتم حفظ المستند بتنسيق PDF، أو إلى صورة، أو طباعته لأول مرة تلقائيًا
// تخزين تخطيط المستند داخل صفحاته.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//تعديل المستند بطريقة ما.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// في الإصدار الحالي من Aspose.Words، لا يؤدي تعديل المستند إلى إعادة البناء تلقائيًا
// تخطيط الصفحة المُخزّن مؤقتًا. إذا أردنا تخطيطًا مُخزّنًا مؤقتًا
//للبقاء على اطلاع، سوف نحتاج إلى تحديثه يدويًا.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

يوضح كيفية إعداد عقدة قسم جديدة للتحرير.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة على قسم يحتوي على نص، والذي بدوره يحتوي على فقرة.
// يمكننا إضافة محتويات إلى هذا المستند عن طريق إضافة عناصر مثل النصوص أو الأشكال أو الجداول إلى تلك الفقرة.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// إذا أضفنا قسمًا جديدًا مثل هذا، فلن يحتوي على نص أو أي عقدة فرعية أخرى.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// قم بتشغيل طريقة "EnsureMinimum" لإضافة نص ونص إلى هذا القسم لبدء تحريره.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Section](../../section/)
* class [SectionCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
