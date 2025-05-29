---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words لـ .NET
description: اطبع مستندك بالكامل بسهولة على طابعتك الافتراضية باستخدام طريقة طباعة المستندات المبسطة لدينا. استمتع بطباعة سريعة وسهلة!
type: docs
weight: 680
url: /ar/net/aspose.words/document/print/
---
## Print() {#print}

يطبع المستند بأكمله على الطابعة الافتراضية.

```csharp
public void Print()
```

## أمثلة

يوضح كيفية طباعة مستند باستخدام الطابعة الافتراضية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// فيما يلي طريقتان لطباعة مستندنا.
// 1 - الطباعة باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد الطابعة التي نرغب في طباعة المستند بها بالاسم:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

اطبع المستند بأكمله على الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم).

```csharp
public void Print(string printerName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerName | String | اسم الطابعة. |

## أمثلة

يوضح كيفية طباعة مستند باستخدام الطابعة الافتراضية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// فيما يلي طريقتان لطباعة مستندنا.
// 1 - الطباعة باستخدام الطابعة الافتراضية:
doc.Print();

// 2 - حدد الطابعة التي نرغب في طباعة المستند بها بالاسم:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم).

```csharp
public void Print(PrinterSettings printerSettings)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة التي سيتم استخدامها. |

## ملاحظات

الPrinterSettings يسمح لك الكائن بتحديد الطابعة التي سيتم الطباعة عليها، ونطاق الصفحات التي سيتم طباعتها وخيارات أخرى.

## أمثلة

يوضح كيفية طباعة مجموعة من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل كيفية طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// اضبط خاصية "PrintRange" على "PrintRange.SomePages" لـ
// أخبر الطابعة بأننا نعتزم طباعة بعض صفحات المستند فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// قم بتعيين الخاصية "FromPage" إلى "1"، والخاصية "ToPage" إلى "3" لطباعة الصفحات من 1 إلى 3.
// فهرسة الصفحة تعتمد على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة مستندنا.
// 1 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا:
doc.Print(printerSettings);

// 2 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا، مع مراعاة أيضًا
// إعطاء المستند اسمًا مخصصًا يمكننا التعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

يطبع المستند وفقًا لإعدادات الطابعة المحددة، باستخدام وحدة التحكم في الطباعة القياسية (بدون واجهة مستخدم) واسم المستند.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| printerSettings | PrinterSettings | إعدادات الطابعة التي سيتم استخدامها. |
| documentName | String | اسم المستند الذي سيتم عرضه (على سبيل المثال، في مربع حوار حالة الطباعة أو قائمة انتظار الطابعة) أثناء طباعة المستند. |

## ملاحظات

الPrinterSettings يسمح لك الكائن بتحديد الطابعة التي سيتم الطباعة عليها، ونطاق الصفحات التي سيتم طباعتها وخيارات أخرى.

## أمثلة

يوضح كيفية طباعة مجموعة من الصفحات.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PrinterSettings" لتعديل كيفية طباعة المستند.
PrinterSettings printerSettings = new PrinterSettings();

// اضبط خاصية "PrintRange" على "PrintRange.SomePages" لـ
// أخبر الطابعة بأننا نعتزم طباعة بعض صفحات المستند فقط.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// قم بتعيين الخاصية "FromPage" إلى "1"، والخاصية "ToPage" إلى "3" لطباعة الصفحات من 1 إلى 3.
// فهرسة الصفحة تعتمد على 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// فيما يلي طريقتان لطباعة مستندنا.
// 1 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا:
doc.Print(printerSettings);

// 2 - الطباعة أثناء تطبيق إعدادات الطباعة لدينا، مع مراعاة أيضًا
// إعطاء المستند اسمًا مخصصًا يمكننا التعرف عليه في قائمة انتظار الطابعة:
doc.Print(printerSettings, "My rendered document");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
