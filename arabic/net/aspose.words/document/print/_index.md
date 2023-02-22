---
title: Document.Print
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. طباعة المستند بالكامل على الطابعة الافتراضية.
type: docs
weight: 620
url: /ar/net/aspose.words/document/print/
---
## Print() {#print}

طباعة المستند بالكامل على الطابعة الافتراضية.

```csharp
public void Print()
```

### أمثلة

يوضح كيفية طباعة مستند باستخدام الطابعة الافتراضية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - اطبع باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد طابعة نرغب في طباعة المستند بالاسم:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Print(string) {#print_3}

اطبع المستند بالكامل على الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم).

```csharp
public void Print(string printerName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerName | String | اسم الطابعة. |

### أمثلة

يوضح كيفية طباعة مستند باستخدام الطابعة الافتراضية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - اطبع باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد طابعة نرغب في طباعة المستند بالاسم:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

طباعة المستند وفقًا لإعدادات الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم).

```csharp
public void Print(PrinterSettings printerSettings)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة المراد استخدامها. |

### ملاحظات

الPrinterSettings يتيح لك كائن تحديد الطابعة التي تريد الطباعة عليها ، ونطاق الصفحات المطلوب طباعتها وخيارات أخرى.

### أمثلة

يوضح كيفية طباعة نطاق من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل طريقة طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// قم بتعيين خاصية "PrintRange" على "PrintRange.SomePages" إلى
// أخبر الطابعة بأننا نعتزم طباعة بعض صفحات المستندات فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// عيّن خاصية "FromPage" على "1" وخاصية "ToPage" على "3" لطباعة الصفحات من 1 إلى 3.
// تعتمد فهرسة الصفحة على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - اطبع أثناء تطبيق إعدادات الطباعة الخاصة بنا:
doc.Print(printerSettings);

// 2 - اطبع أثناء تطبيق إعدادات الطباعة الخاصة بنا ، بينما أيضًا
// إعطاء المستند اسمًا مخصصًا قد نتعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

طباعة المستند وفقًا لإعدادات الطابعة المحددة ، باستخدام وحدة تحكم الطباعة القياسية (بدون واجهة مستخدم) واسم المستند.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة المراد استخدامها. |
| documentName | String | اسم المستند المراد عرضه (على سبيل المثال ، في مربع حوار حالة الطباعة_ أو قائمة انتظار الطابعة) أثناء طباعة المستند. |

### ملاحظات

الPrinterSettings يتيح لك كائن تحديد الطابعة التي تريد الطباعة عليها ، ونطاق الصفحات المطلوب طباعتها وخيارات أخرى.

### أمثلة

يوضح كيفية طباعة نطاق من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل طريقة طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// قم بتعيين خاصية "PrintRange" على "PrintRange.SomePages" إلى
// أخبر الطابعة بأننا نعتزم طباعة بعض صفحات المستندات فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// عيّن خاصية "FromPage" على "1" وخاصية "ToPage" على "3" لطباعة الصفحات من 1 إلى 3.
// تعتمد فهرسة الصفحة على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - اطبع أثناء تطبيق إعدادات الطباعة الخاصة بنا:
doc.Print(printerSettings);

// 2 - اطبع أثناء تطبيق إعدادات الطباعة الخاصة بنا ، بينما أيضًا
// إعطاء المستند اسمًا مخصصًا قد نتعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


