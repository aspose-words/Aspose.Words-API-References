---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words لـ .NET
description: قم بإجراء دمج بريدي بسهولة للسجلات الفردية وتحويل النتائج إلى صور عالية الجودة باستخدام طريقة MailMerger ExecuteToImages.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

ينفذ عملية دمج البريد لسجل واحد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| fieldNames | String[] | مجموعة من أسماء حقول الدمج. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| fieldValues | Object[] | مصفوفة القيم المراد إدراجها في حقول الدمج. يجب أن يكون عدد عناصر هذه المصفوفة مساويًا لعدد عناصر أسماء الحقول. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد لسجل واحد وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

ينفذ عملية دمج البريد لسجل واحد ويعرض النتيجة على شكل صور.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| fieldNames | String[] | مجموعة من أسماء حقول الدمج. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| fieldValues | Object[] | مصفوفة القيم المراد إدراجها في حقول الدمج. يجب أن يكون عدد عناصر هذه المصفوفة مساويًا لعدد عناصر أسماء الحقول. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد لسجل واحد من التدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد باستخدام المستندات من التدفق:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

يقوم بدمج البريد من صف بيانات إلى المستند ويعرض النتيجة على الصور.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataRow | DataRow | صف يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد من DataRow وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

يقوم بدمج البريد من صف بيانات إلى المستند ويعرض النتيجة على الصور.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataRow | DataRow | صف يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد من DataRow باستخدام المستندات من التدفق وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من DataRow باستخدام المستندات من التدفق:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

يقوم بدمج البريد من صف بيانات إلى المستند ويعرض النتيجة على الصور.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataTable | DataTable | جدول يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد من جدول البيانات وحفظ النتيجة في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من جدول البيانات:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

يقوم بدمج البريد من صف بيانات إلى المستند ويعرض النتيجة على الصور.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات حفظ الإخراج. |
| dataTable | DataTable | جدول يحتوي على بيانات لإدراجها في حقول دمج البريد. أسماء الحقول لا تراعي حالة الأحرف. في حال وجود اسم حقل غير موجود في المستند، فسيتم تجاهله. |
| mailMergeOptions | MailMergeOptions | خيارات دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق وحفظها في الصور.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق وحفظ النتيجة في الصور:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
