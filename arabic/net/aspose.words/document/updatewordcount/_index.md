---
title: Document.UpdateWordCount
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. لتحديث خصائص عدد الكلمات في المستند.
type: docs
weight: 810
url: /ar/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

لتحديث خصائص عدد الكلمات في المستند.

```csharp
public void UpdateWordCount()
```

### ملاحظات

`UpdateWordCount` يعيد حساب وتحديث خصائص الأحرف والكلمات والفقرات في ملف[`BuiltInDocumentProperties`](../builtindocumentproperties/) جمع من[`Document`](../).

لاحظ أن`UpdateWordCount`لا يقوم بتحديث خصائص عدد الأسطر والصفحات. استخدم`UpdateWordCount` الزائد وتمرير`حقيقي` القيمة كمعلمة للقيام بذلك.

عند استخدام إصدار تقييمي، سيتم أيضًا تضمين العلامة المائية للتقييم في عدد الكلمات.

### أمثلة

يوضح كيفية تحديث جميع تسميات القائمة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words لا يتتبع مقاييس المستند مثل هذه في الوقت الفعلي.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// للحصول على قيم دقيقة لثلاث من هذه الخصائص، سنحتاج إلى تحديثها يدويًا.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// بالنسبة لعدد الأسطر، سنحتاج إلى استدعاء تحميل زائد محدد لطريقة التحديث.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## UpdateWordCount(bool) {#updatewordcount_1}

يقوم بتحديث خصائص عدد الكلمات في المستند، ويتم تحديثه بشكل اختياري[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) الملكية.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| updateLinesCount | Boolean | `حقيقي` إذا تم حساب عدد الأسطر في الوثيقة. |

### ملاحظات

ستعمل هذه الطريقة على إعادة بناء تخطيط صفحة المستند.

### أمثلة

يوضح كيفية تحديث جميع تسميات القائمة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words لا يتتبع مقاييس المستند مثل هذه في الوقت الفعلي.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// للحصول على قيم دقيقة لثلاث من هذه الخصائص، سنحتاج إلى تحديثها يدويًا.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// بالنسبة لعدد الأسطر، سنحتاج إلى استدعاء تحميل زائد محدد لطريقة التحديث.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


