---
title: CleanupOptions.UnusedBuiltinStyles
second_title: Aspose.Words لمراجع .NET API
description: CleanupOptions ملكية. يحدد ما هو غير مستخدمBuiltIn يجب إزالة الأنماط من المستند.
type: docs
weight: 30
url: /ar/net/aspose.words/cleanupoptions/unusedbuiltinstyles/
---
## CleanupOptions.UnusedBuiltinStyles property

يحدد ما هو غير مستخدم[`BuiltIn`](../../style/builtin/) يجب إزالة الأنماط من المستند.

```csharp
public bool UnusedBuiltinStyles { get; set; }
```

### أمثلة

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

* class [CleanupOptions](../)
* مساحة الاسم [Aspose.Words](../../cleanupoptions/)
* المجسم [Aspose.Words](../../../)


