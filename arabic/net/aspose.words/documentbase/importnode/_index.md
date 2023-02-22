---
title: DocumentBase.ImportNode
second_title: Aspose.Words لمراجع .NET API
description: DocumentBase طريقة. يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية.
type: docs
weight: 100
url: /ar/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة التي يتم استيرادها. |
| isImportChildren | Boolean | صحيح لاستيراد جميع العقد الفرعية بشكل متكرر ؛ خلاف ذلك ، خطأ. |

### قيمة الإرجاع

العقدة المستنسخة التي تنتمي إلى المستند الحالي.

### ملاحظات

تستخدم هذه الطريقة الامتدادUseDestinationStyles خيار لحل التنسيق.

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر تنتمي إلى المستند المستورد. العقدة التي تم إرجاعها ليس لها أصل. لم يتم تغيير عقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند ، يجب استيرادها . أثناء الاستيراد ، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم_ من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة ، يمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة ، فسيتم إنشاء نسخة عميقة من العقدة المصدر.

### أمثلة

يوضح كيفية استيراد عقدة من مستند إلى آخر.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// تحتوي كل عقدة على مستند أصلي ، وهو المستند الذي يحتوي على العقدة.
// سيؤدي إدخال عقدة في مستند لا تنتمي إليه العقدة إلى طرح استثناء.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// استخدم طريقة ImportNode لإنشاء نسخة من العقدة ، والتي سيكون لها المستند
// التي تسمى طريقة ImportNode التي تم تعيينها كمستند مالك جديد.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// يمكننا الآن إدخال العقدة في المستند.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### أنظر أيضا

* class [Node](../../node/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../documentbase/)
* المجسم [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

يستورد عقدة من وثيقة أخرى إلى الوثيقة الحالية مع خيار للتحكم في التنسيق.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة المراد استيرادها. |
| isImportChildren | Boolean | صحيح لاستيراد جميع العقد الفرعية بشكل متكرر ؛ خلاف ذلك ، خطأ. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |

### قيمة الإرجاع

العقدة المستنسخة والمستوردة. تنتمي العقدة إلى المستند الوجهة ، ولكن ليس لها أصل.

### ملاحظات

هذا التحميل الزائد مفيد للتحكم في كيفية استيراد الأنماط وتنسيق القائمة.

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر تنتمي إلى المستند المستورد. العقدة التي تم إرجاعها ليس لها أصل. لم يتم تغيير عقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند ، يجب استيرادها . أثناء الاستيراد ، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم_ من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة ، يمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة ، فسيتم إنشاء نسخة عميقة من العقدة المصدر.

### أمثلة

يوضح كيفية استيراد عقدة من المستند المصدر إلى المستند الوجهة بخيارات محددة.

```csharp
// قم بإنشاء وثيقتين وأضف نمط حرف إلى كل مستند.
// تكوين الأنماط ليكون لها نفس الاسم ، ولكن تنسيق نص مختلف.
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

// استيراد القسم من المستند الوجهة إلى المستند المصدر ، مما يتسبب في تضارب اسم النمط.
// إذا استخدمنا أنماط الوجهة ، فإن النص المصدر الذي تم استيراده يحمل نفس اسم النمط
// كنص وجهة ستتبنى نمط الوجهة.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// إذا استخدمنا ImportFormatMode.KeepDifferentStyles ، فسيتم الاحتفاظ بنمط المصدر ،
// ويحل تعارض التسمية بإضافة لاحقة.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### أنظر أيضا

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../documentbase/)
* المجسم [Aspose.Words](../../../)


