---
title: Document.Print
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. طباعة المستند بالكامل إلى الطابعة الافتراضية.
type: docs
weight: 660
url: /ar/net/aspose.words/document/print/
---
## Print() {#print}

طباعة المستند بالكامل إلى الطابعة الافتراضية.

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
// 1 - الطباعة باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد الطابعة التي نرغب في طباعة المستند بها بالاسم:
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

طباعة المستند بالكامل إلى الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم).

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
// 1 - الطباعة باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد الطابعة التي نرغب في طباعة المستند بها بالاسم:
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

يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم).

```csharp
public void Print(PrinterSettings printerSettings)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة المراد استخدامها. |

### ملاحظات

الPrinterSettings يتيح لك كائن تحديد الطابعة التي تريد الطباعة عليها، ونطاق الصفحات التي تريد طباعتها، والخيارات الأخرى.

### أمثلة

يوضح كيفية طباعة مجموعة من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل كيفية طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// قم بتعيين خاصية "PrintRange" على "PrintRange.SomePages" إلى
// أخبر الطابعة أننا نعتزم طباعة بعض صفحات المستندات فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// اضبط الخاصية "FromPage" على "1"، والخاصية "ToPage" على "3" لطباعة الصفحات من 1 إلى 3.
// فهرسة الصفحة تعتمد على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - الطباعة أثناء تطبيق إعدادات الطباعة الخاصة بنا:
doc.Print(printerSettings);

// 2 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا، بينما أيضًا
// إعطاء المستند اسمًا مخصصًا قد نتعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم) واسم المستند.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة المراد استخدامها. |
| documentName | String | اسم المستند الذي سيتم عرضه (على سبيل المثال، في مربع حوار حالة الطباعة أو قائمة انتظار الطابعة) أثناء طباعة المستند. |

### ملاحظات

الPrinterSettings يتيح لك كائن تحديد الطابعة التي تريد الطباعة عليها، ونطاق الصفحات التي تريد طباعتها، والخيارات الأخرى.

### أمثلة

يوضح كيفية طباعة مجموعة من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل كيفية طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// قم بتعيين خاصية "PrintRange" على "PrintRange.SomePages" إلى
// أخبر الطابعة أننا نعتزم طباعة بعض صفحات المستندات فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// اضبط الخاصية "FromPage" على "1"، والخاصية "ToPage" على "3" لطباعة الصفحات من 1 إلى 3.
// فهرسة الصفحة تعتمد على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة وثيقتنا.
// 1 - الطباعة أثناء تطبيق إعدادات الطباعة الخاصة بنا:
doc.Print(printerSettings);

// 2 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا، بينما أيضًا
// إعطاء المستند اسمًا مخصصًا قد نتعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


