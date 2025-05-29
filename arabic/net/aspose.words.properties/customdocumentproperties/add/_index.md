---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: أنشئ خصائص مستندات مخصصة وفريدة بسهولة باستخدام طريقة الإضافة. حسّن مستنداتك بأنواع بيانات سلسلة نصية مُخصصة لتحقيق أداء مثالي.
type: docs
weight: 10
url: /ar/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

ينشئ خاصية مستند مخصصة جديدة لـString نوع البيانات.

```csharp
public DocumentProperty Add(string name, string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | String | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

ينشئ خاصية مستند مخصصة جديدة لـNumber نوع البيانات.

```csharp
public DocumentProperty Add(string name, int value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Int32 | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

ينشئ خاصية مستند مخصصة جديدة لـDateTime نوع البيانات.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | DateTime | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

## أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على تاريخ ووقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

ينشئ خاصية مستند مخصصة جديدة لـBoolean نوع البيانات.

```csharp
public DocumentProperty Add(string name, bool value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Boolean | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

ينشئ خاصية مستند مخصصة جديدة لـDouble نوع البيانات.

```csharp
public DocumentProperty Add(string name, double value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Double | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة حسب الترتيب الأبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

//طباعة كل خاصية مخصصة في المستند.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// عرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" -> "خصائص" > "خصائص متقدمة" > "مخصص".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من المستند.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
