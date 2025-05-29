---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: Aspose.Words لـ .NET
description: قم بدمج البيانات بسهولة من جدول بيانات في المستندات باستخدام MailMerger ExecuteWithRegionsToImages، مما يحول المحتوى الخاص بك إلى صور مذهلة.
type: docs
weight: 50
url: /ar/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

يقوم بإجراء دمج البريد من جدول بيانات إلى المستند الذي يحتوي على مناطق دمج البريد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataTable | DataTable | جدول يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية القيام بعملية دمج البريد مع المناطق من جدول البيانات وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من جدول البيانات:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

يقوم بإجراء دمج البريد من جدول بيانات إلى المستند الذي يحتوي على مناطق دمج البريد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataTable | DataTable | جدول يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية القيام بعملية دمج البريد مع المناطق من جدول بيانات باستخدام المستندات من التدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من جدول بيانات باستخدام المستندات من التدفق:
DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

يقوم بتنفيذ دمج البريد من مجموعة بيانات إلى المستند الذي يحتوي على مناطق دمج البريد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataSet | DataSet | مجموعة البيانات التي تحتوي على البيانات التي سيتم إدراجها في حقول دمج البريد. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية القيام بعملية دمج البريد مع المناطق من مجموعة بيانات وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من مجموعة البيانات:
string doc = MyDir + "Mail merge with regions data set.docx";

DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

يقوم بتنفيذ دمج البريد من مجموعة بيانات إلى المستند الذي يحتوي على مناطق دمج البريد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataSet | DataSet | مجموعة البيانات التي تحتوي على البيانات التي سيتم إدراجها في حقول دمج البريد. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية القيام بعملية دمج البريد مع المناطق من مجموعة بيانات باستخدام المستندات من التدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من مجموعة بيانات باستخدام المستندات من التدفق:
DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
