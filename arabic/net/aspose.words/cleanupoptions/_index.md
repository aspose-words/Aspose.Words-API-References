---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.CleanupOptions فصل. يسمح بتحديد خيارات تنظيف المستندات في C#.
type: docs
weight: 210
url: /ar/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

يسمح بتحديد خيارات تنظيف المستندات.

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
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | الحصول على/تعيين علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي`خطأ شنيع` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | يحدد ما هو غير مستخدم[`BuiltIn`](../style/builtin/) يجب إزالة الأنماط من المستند. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | يحدد ما إذا كان يجب إزالة القائمة غير المستخدمة وتعريفات القائمة من المستند. القيمة الافتراضية هي`حقيقي` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | يحدد ما إذا كان يجب إزالة الأنماط غير المستخدمة من المستند. القيمة الافتراضية هي`حقيقي` . |

## أمثلة

يوضح كيفية إزالة جميع الأنماط المخصصة غير المستخدمة من المستند.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// بالدمج مع الأنماط المضمنة، أصبح المستند الآن يحتوي على ثمانية أنماط.
// يتم وضع علامة على النمط المخصص على أنه "مستخدم" أثناء وجود أي نص داخل المستند
// منسق بهذا النمط. وهذا يعني أن الأنماط الأربعة التي أضفناها غير مستخدمة حاليًا.
Assert.AreEqual(8, doc.Styles.Count);

// قم بتطبيق نمط أحرف مخصص، ثم نمط قائمة مخصص. سيؤدي القيام بذلك إلى وضع علامة "مستخدمة" عليها.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// الآن، يوجد نمط أحرف واحد غير مستخدم ونمط قائمة واحد غير مستخدم.
// يمكن لأسلوب Cleanup()، عند تكوينه باستخدام كائن CleanupOptions، استهداف الأنماط غير المستخدمة وإزالتها.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // إزالة كل عقدة يتم تطبيق نمط مخصص عليها لوضع علامة عليها على أنها "غير مستخدمة" مرة أخرى.
// أعد تشغيل طريقة التنظيف لإزالتها.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
