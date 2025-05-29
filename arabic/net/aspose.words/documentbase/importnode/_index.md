---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words لـ .NET
description: استورد العقد بسهولة من مستندات أخرى لتحسين سير عملك باستخدام طريقة ImportNode من DocumentBase. بسّط إدارة مستنداتك اليوم!
type: docs
weight: 110
url: /ar/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

استيراد عقدة من مستند آخر إلى المستند الحالي.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة التي يتم استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا،`خطأ شنيع`. |

### قيمة الإرجاع

العقدة المستنسخة التي تنتمي إلى المستند الحالي.

## ملاحظات

تستخدم هذه الطريقةUseDestinationStyles خيار لحل التنسيق.

استيراد عقدة يُنشئ نسخة من العقدة المصدرية للمستند المُستورد. العقدة المُعادة ليس لها أصل. العقدة المصدرية لم تُعدّل أو تُزال من المستند الأصلي.

قبل إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند، مثل مراجع الأنماط والقوائم، من المستند الأصلي إلى المستند المُستورد. بعد استيراد العقدة، يُمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء clone عميق للعقدة المصدر.

## أمثلة

يوضح كيفية استيراد عقدة من مستند إلى آخر.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// كل عقدة لديها مستند رئيسي، وهو المستند الذي يحتوي على العقدة.
// إدراج عقدة في مستند لا تنتمي إليه العقدة سيؤدي إلى حدوث استثناء.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// استخدم طريقة ImportNode لإنشاء نسخة من العقدة، والتي ستحتوي على المستند
// الذي استدعى مجموعة طريقة ImportNode كمستند مالك جديد.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

//يمكننا الآن إدراج العقدة في المستند.
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

استيراد عقدة من مستند آخر إلى المستند الحالي مع خيار التحكم في التنسيق.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة المراد استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا،`خطأ شنيع`. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |

### قيمة الإرجاع

العقدة المُستنسخة والمُستوردة. تنتمي هذه العقدة إلى مستند الوجهة، ولكن ليس لها عقدة رئيسية.

## ملاحظات

يعد هذا التحميل الزائد مفيدًا للتحكم في كيفية استيراد الأنماط وتنسيق القائمة.

استيراد عقدة يُنشئ نسخة من العقدة المصدرية للمستند المُستورد. العقدة المُعادة ليس لها أصل. العقدة المصدرية لم تُعدّل أو تُزال من المستند الأصلي.

قبل إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند، مثل مراجع الأنماط والقوائم، من المستند الأصلي إلى المستند المُستورد. بعد استيراد العقدة، يُمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء clone عميق للعقدة المصدر.

## أمثلة

يوضح كيفية استيراد العقدة من مستند المصدر إلى مستند الوجهة باستخدام خيارات محددة.

```csharp
// قم بإنشاء مستندين وأضف نمطًا للأحرف إلى كل مستند.
// قم بتكوين الأنماط بحيث يكون لها نفس الاسم، ولكن تنسيق نص مختلف.
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

// استيراد القسم من المستند الوجهة إلى المستند المصدر، مما يتسبب في حدوث تعارض في اسم النمط.
// إذا استخدمنا أنماط الوجهة، فسيتم استيراد النص المصدر بنفس اسم النمط
// حيث سيعتمد النص الوجهة نمط الوجهة.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// إذا استخدمنا ImportFormatMode.KeepDifferentStyles، فسيتم الحفاظ على نمط المصدر،
// ويتم حل صراع التسمية عن طريق إضافة لاحقة.
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
