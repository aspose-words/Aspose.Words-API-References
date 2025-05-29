---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words for .NET
description: 使用我们精简的文档打印方法，轻松将整个文档打印到您的默认打印机。享受快速、轻松的打印体验！
type: docs
weight: 680
url: /zh/net/aspose.words/document/print/
---
## Print() {#print}

将整个文档打印到默认打印机。

```csharp
public void Print()
```

## 例子

展示如何使用默认打印机打印文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 以下是打印文档的两种方法。
// 1 - 使用默认打印机打印：
doc.Print();

// 2 - 通过名称指定我们希望用来打印文档的打印机：
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

将整个文档打印到指定的打印机， 使用标准（无用户界面）打印控制器。

```csharp
public void Print(string printerName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerName | String | 打印机的名称。 |

## 例子

展示如何使用默认打印机打印文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 以下是打印文档的两种方法。
// 1 - 使用默认打印机打印：
doc.Print();

// 2 - 通过名称指定我们希望用来打印文档的打印机：
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器。

```csharp
public void Print(PrinterSettings printerSettings)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | PrinterSettings | 要使用的打印机设置。 |

## 评论

这PrinterSettings 对象允许您指定要打印的打印机、要打印的页面范围和其他选项。

## 例子

展示如何打印一系列页面。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“PrinterSettings”对象来修改我们打印文档的方式。
PrinterSettings printerSettings = new PrinterSettings();

// 将“PrintRange”属性设置为“PrintRange.SomePages”
// 告诉打印机我们只想打印一些文档页面。
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 将“FromPage”属性设置为“1”，将“ToPage”属性设置为“3”，以打印第 1 至第 3 页。
// 页面索引以 1 为基础。
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// 以下是打印文档的两种方法。
// 1 - 应用我们的打印设置进行打印：
doc.Print(printerSettings);

// 2 - 在应用我们的打印设置的同时进行打印，同时
// 为文档提供一个我们可以在打印机队列中识别的自定义名称：
doc.Print(printerSettings, "My rendered document");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器和文档名称。

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| printerSettings | PrinterSettings | 要使用的打印机设置。 |
| documentName | String | 打印文档时显示的文档名称（例如，在打印状态 dialog 框或打印机队列中）。 |

## 评论

这PrinterSettings 对象允许您指定要打印的打印机、要打印的页面范围和其他选项。

## 例子

展示如何打印一系列页面。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“PrinterSettings”对象来修改我们打印文档的方式。
PrinterSettings printerSettings = new PrinterSettings();

// 将“PrintRange”属性设置为“PrintRange.SomePages”
// 告诉打印机我们只想打印一些文档页面。
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// 将“FromPage”属性设置为“1”，将“ToPage”属性设置为“3”，以打印第 1 至第 3 页。
// 页面索引以 1 为基础。
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// 以下是打印文档的两种方法。
// 1 - 应用我们的打印设置进行打印：
doc.Print(printerSettings);

// 2 - 在应用我们的打印设置的同时进行打印，同时
// 为文档提供一个我们可以在打印机队列中识别的自定义名称：
doc.Print(printerSettings, "My rendered document");
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
