---
title: Add
second_title: Aspose.Words لمراجع .NET API
description: إنشاء خاصية مستند مخصصة جديدة لملف PropertyType.String نوع البيانات ._ x000d_
type: docs
weight: 10
url: /ar/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(string, string) {#add_4}

إنشاء خاصية مستند مخصصة جديدة لملف **PropertyType.String** نوع البيانات ._ x000d_

```csharp
public DocumentProperty Add(string name, string value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | String | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../customdocumentproperties)
* المجسم [Aspose.Words](../../../)

---

## Add(string, int) {#add_2}

إنشاء خاصية مستند مخصصة جديدة لملف **نوع الملكية** نوع البيانات ._ x000d_

```csharp
public DocumentProperty Add(string name, int value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Int32 | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../customdocumentproperties)
* المجسم [Aspose.Words](../../../)

---

## Add(string, DateTime) {#add_3}

إنشاء خاصية مستند مخصصة جديدة لملف **PropertyType.DateTime** نوع البيانات ._ x000d_

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | DateTime | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

### أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على التاريخ والوقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../customdocumentproperties)
* المجسم [Aspose.Words](../../../)

---

## Add(string, bool) {#add}

إنشاء خاصية مستند مخصصة جديدة لملف **نوع الملكية. منطقي** نوع البيانات ._ x000d_

```csharp
public DocumentProperty Add(string name, bool value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Boolean | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../customdocumentproperties)
* المجسم [Aspose.Words](../../../)

---

## Add(string, double) {#add_1}

إنشاء خاصية مستند مخصصة جديدة لملف **نوع الملكية** نوع البيانات ._ x000d_

```csharp
public DocumentProperty Add(string name, double value)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| value | Double | قيمة العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا.

### أمثلة

يوضح كيفية التعامل مع الخصائص المخصصة للمستند.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// خصائص المستند المخصصة هي أزواج ذات قيمة رئيسية يمكننا إضافتها إلى المستند.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// تقوم المجموعة بفرز الخصائص المخصصة بترتيب أبجدي.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// طباعة كل خاصية مخصصة في المستند.
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

// يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "ملف" - >; "خصائص" >. "خصائص متقدمة" >. "العادة".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// فيما يلي ثلاث طرق أو إزالة الخصائص المخصصة من مستند.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - إفراغ المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../customdocumentproperties)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
