---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words لـ .NET
description: قم بتعزيز كفاءة مستندك باستخدام طريقة UpdateWordCount، مما يضمن خصائص عدد الكلمات الدقيقة لتحسين التحرير والمراجعة.
type: docs
weight: 850
url: /ar/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

تحديث خصائص عدد الكلمات في المستند.

```csharp
public void UpdateWordCount()
```

## ملاحظات

`UpdateWordCount` يعيد حساب وتحديث خصائص الأحرف والكلمات والفقرات في[`BuiltInDocumentProperties`](../builtindocumentproperties/) مجموعة من[`Document`](../).

لاحظ أن`UpdateWordCount` لا يتم تحديث عدد الأسطر وخصائص الصفحات. استخدم`UpdateWordCount` التحميل الزائد والتمرير`حقيقي` القيمة كمعلمة للقيام بذلك.

عند استخدام إصدار التقييم، سيتم أيضًا تضمين العلامة المائية للتقييم في عدد الكلمات.

## أمثلة

يوضح كيفية تحديث كافة تسميات القائمة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// لا يتتبع Aspose.Words مقاييس المستندات مثل هذه في الوقت الفعلي.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

تحديث خصائص عدد الكلمات في المستند، ويتم التحديث بشكل اختياري[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) الملكية.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| updateLinesCount | Boolean | `حقيقي` إذا كان من المفترض حساب عدد الأسطر في المستند. |

## ملاحظات

ستعمل هذه الطريقة على إعادة بناء تخطيط الصفحة للمستند.

## أمثلة

يوضح كيفية تحديث كافة تسميات القائمة في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// لا يتتبع Aspose.Words مقاييس المستندات مثل هذه في الوقت الفعلي.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
