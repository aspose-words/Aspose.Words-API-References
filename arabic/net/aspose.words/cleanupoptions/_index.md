---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.Cleanup لتخصيص تنظيف المستندات. حسّن سير عملك بإعدادات مُخصصة لمستندات أكثر نظافة وكفاءة.
type: docs
weight: 400
url: /ar/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

يسمح بتحديد خيارات لتنظيف المستندات.

لمعرفة المزيد، قم بزيارة[تنظيف مستند](https://docs.aspose.com/words/net/clean-up-a-document/) مقالة توثيقية.

```csharp
public class CleanupOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | يحصل على/يعين علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي`خطأ شنيع` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | يحدد أنه غير مستخدم[`BuiltIn`](../style/builtin/) يجب إزالة الأنماط من المستند. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | يحدد ما إذا كان يجب إزالة القائمة غير المستخدمة وتعريفات القائمة من المستند. القيمة الافتراضية هي`حقيقي` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. القيمة الافتراضية هي`حقيقي` . |

## أمثلة

يوضح كيفية إزالة كافة الأنماط المخصصة غير المستخدمة من مستند.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// مع دمج الأنماط المضمنة، أصبح لدى المستند الآن ثمانية أنماط.
// يتم وضع علامة على النمط المخصص على أنه "مستخدم" أثناء وجود أي نص داخل المستند
// مُنسّق بهذا النمط. هذا يعني أن الأنماط الأربعة التي أضفناها غير مُستخدمة حاليًا.
Assert.AreEqual(8, doc.Styles.Count);

// طبّق نمط حرف مخصص، ثم نمط قائمة مخصص. سيؤدي ذلك إلى تمييزهما بعلامة "مستخدم".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// الآن، هناك نمط حرف واحد غير مستخدم ونمط قائمة واحد غير مستخدم.
// عند تكوين طريقة Cleanup() باستخدام كائن CleanupOptions، يمكنها استهداف الأنماط غير المستخدمة وإزالتها.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // يؤدي إزالة كل عقدة تم تطبيق نمط مخصص عليها إلى تمييزها بأنها "غير مستخدمة" مرة أخرى.
// أعد تشغيل طريقة التنظيف لإزالتها.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
