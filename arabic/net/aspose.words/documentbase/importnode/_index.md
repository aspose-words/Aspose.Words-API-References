---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words لـ .NET
description: DocumentBase ImportNode طريقة. يستورد عقدة من مستند آخر إلى المستند الحالي في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

يستورد عقدة من مستند آخر إلى المستند الحالي.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة التي يتم استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد كافة العقد التابعة بشكل متكرر؛ خلاف ذلك،`خطأ شنيع`. |

### قيمة الإرجاع

العقدة المستنسخة التي تنتمي إلى الوثيقة الحالية.

## ملاحظات

تستخدم هذه الطريقةUseDestinationStyles خيار لحل التنسيق.

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر التي تنتمي إلى مستند الاستيراد. العقدة التي تم إرجاعها ليس لها أصل. لا يتم تغيير العقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة، يمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء استنساخ عميق للعقدة المصدر.

## أمثلة

يوضح كيفية استيراد عقدة من مستند إلى آخر.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// تحتوي كل عقدة على مستند أصل، وهو المستند الذي يحتوي على العقدة.
// سيؤدي إدراج عقدة في مستند لا تنتمي إليه العقدة إلى حدوث استثناء.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// استخدم طريقة ImportNode لإنشاء نسخة من العقدة التي ستحتوي على المستند
// الذي تم تعيين أسلوب ImportNode كمستند المالك الجديد له.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// يمكننا الآن إدراج العقدة في المستند.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### أنظر أيضا

* class [Node](../../node/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار التحكم في التنسيق.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة المراد استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد كافة العقد التابعة بشكل متكرر؛ خلاف ذلك،`خطأ شنيع`. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات النمط التي تتعارض. |

### قيمة الإرجاع

العقدة المستنسخة والمستوردة. تنتمي العقدة إلى المستند الوجهة، ولكن ليس لها أصل.

## ملاحظات

يعد هذا التحميل الزائد مفيدًا للتحكم في كيفية استيراد الأنماط وتنسيقات القائمة.

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر التي تنتمي إلى مستند الاستيراد. العقدة التي تم إرجاعها ليس لها أصل. لا يتم تغيير العقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة، يمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء استنساخ عميق للعقدة المصدر.

## أمثلة

يوضح كيفية استيراد العقدة من المستند المصدر إلى المستند الوجهة بخيارات محددة.

```csharp
// أنشئ مستندين وأضف نمط الأحرف إلى كل مستند.
// قم بتكوين الأنماط بحيث تحمل نفس الاسم، ولكن بتنسيق نص مختلف.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// قم باستيراد القسم من المستند الوجهة إلى المستند المصدر، مما يتسبب في تضارب اسم النمط.
// إذا كنا نستخدم أنماط الوجهة، فإن النص المصدر المستورد يحمل نفس اسم النمط
// كنص الوجهة سيعتمد نمط الوجهة.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// إذا استخدمنا ImportFormatMode.KeepDifferentStyles، فسيتم الحفاظ على النمط المصدر،
// ويتم حل التعارض في التسمية عن طريق إضافة لاحقة.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### أنظر أيضا

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
