---
title: Document.Print
second_title: Aspose.Words for .NET API Reference
description: Document method. Prints the whole document to the default printer in C#
type: docs
weight: 640
url: /net/aspose.words/document/print/
---
## Print() {#print}

Prints the whole document to the default printer.

```csharp
public void Print()
```

## Examples

Shows how to print a document using the default printer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Below are two ways of printing our document.
// 1 -  Print using the default printer:
doc.Print();

// 2 -  Specify a printer that we wish to print the document with by name:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Print the whole document to the specified printer, using the standard (no User Interface) print controller.

```csharp
public void Print(string printerName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| printerName | String | The name of the printer. |

## Examples

Shows how to print a document using the default printer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Below are two ways of printing our document.
// 1 -  Print using the default printer:
doc.Print();

// 2 -  Specify a printer that we wish to print the document with by name:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Prints the document according to the specified printer settings, using the standard (no User Interface) print controller.

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parameter | Type | Description |
| --- | --- | --- |
| printerSettings | PrinterSettings | The printer settings to use. |

## Remarks

The PrinterSettings object allows you to specify the printer to print on, the range of pages of to print and other options.

## Examples

Shows how to print a range of pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create a "PrinterSettings" object to modify how we print the document.
PrinterSettings printerSettings = new PrinterSettings();

// Set the "PrintRange" property to "PrintRange.SomePages" to
// tell the printer that we intend to print only some document pages.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Set the "FromPage" property to "1", and the "ToPage" property to "3" to print pages 1 through to 3.
// Page indexing is 1-based.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Below are two ways of printing our document.
// 1 -  Print while applying our printing settings:
doc.Print(printerSettings);

// 2 -  Print while applying our printing settings, while also
// giving the document a custom name that we may recognize in the printer queue:
doc.Print(printerSettings, "My rendered document");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| printerSettings | PrinterSettings | The printer settings to use. |
| documentName | String | The document name to display (for example, in a print status dialog box or printer queue) while printing the document. |

## Remarks

The PrinterSettings object allows you to specify the printer to print on, the range of pages of to print and other options.

## Examples

Shows how to print a range of pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create a "PrinterSettings" object to modify how we print the document.
PrinterSettings printerSettings = new PrinterSettings();

// Set the "PrintRange" property to "PrintRange.SomePages" to
// tell the printer that we intend to print only some document pages.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Set the "FromPage" property to "1", and the "ToPage" property to "3" to print pages 1 through to 3.
// Page indexing is 1-based.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Below are two ways of printing our document.
// 1 -  Print while applying our printing settings:
doc.Print(printerSettings);

// 2 -  Print while applying our printing settings, while also
// giving the document a custom name that we may recognize in the printer queue:
doc.Print(printerSettings, "My rendered document");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
