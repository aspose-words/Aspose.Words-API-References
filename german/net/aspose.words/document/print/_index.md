---
title: Print
second_title: Aspose.Words für .NET-API-Referenz
description: Druckt das gesamte Dokument auf dem Standarddrucker.
type: docs
weight: 620
url: /de/net/aspose.words/document/print/
---
## Print() {#print}

Druckt das gesamte Dokument auf dem Standarddrucker.

```csharp
public void Print()
```

### Beispiele

Zeigt, wie ein Dokument mit dem Standarddrucker gedruckt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument zu drucken.
// 1 - Drucken mit dem Standarddrucker:
doc.Print();

// 2 - Geben Sie einen Drucker an, mit dem wir das Dokument namentlich drucken möchten:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Drucken Sie das gesamte Dokument auf dem angegebenen Drucker, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche).

```csharp
public void Print(string printerName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerName | String | Der Name des Druckers. |

### Beispiele

Zeigt, wie ein Dokument mit dem Standarddrucker gedruckt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument zu drucken.
// 1 - Drucken mit dem Standarddrucker:
doc.Print();

// 2 - Geben Sie einen Drucker an, mit dem wir das Dokument namentlich drucken möchten:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |

### Bemerkungen

DasPrinterSettings Das -Objekt ermöglicht es Ihnen, den zu druckenden Drucker, den zu druckenden Seitenbereich und andere Optionen anzugeben.

### Beispiele

Zeigt, wie eine Reihe von Seiten gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein "PrinterSettings"-Objekt, um zu ändern, wie wir das Dokument drucken.
PrinterSettings printerSettings = new PrinterSettings();

// Legen Sie die Eigenschaft "PrintRange" auf "PrintRange.SomePages" fest
// dem Drucker mitteilen, dass wir beabsichtigen, nur einige Dokumentseiten zu drucken.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft "FromPage" auf "1" und die Eigenschaft "ToPage" auf "3", um die Seiten 1 bis 3 zu drucken.
// Seitenindizierung ist 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument zu drucken.
// 1 - Drucken, während unsere Druckeinstellungen angewendet werden:
doc.Print(printerSettings);

// 2 - Drucken, während unsere Druckeinstellungen angewendet werden, während auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir in der Druckerwarteschlange erkennen können:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche) und eines Dokumentnamens.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |
| documentName | String | Der Dokumentname, der beim Drucken des Dokuments angezeigt werden soll (z. B. in einem Druckstatusfeld dialog oder einer Druckerwarteschlange). |

### Bemerkungen

DasPrinterSettings Das -Objekt ermöglicht es Ihnen, den zu druckenden Drucker, den zu druckenden Seitenbereich und andere Optionen anzugeben.

### Beispiele

Zeigt, wie eine Reihe von Seiten gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein "PrinterSettings"-Objekt, um zu ändern, wie wir das Dokument drucken.
PrinterSettings printerSettings = new PrinterSettings();

// Legen Sie die Eigenschaft "PrintRange" auf "PrintRange.SomePages" fest
// dem Drucker mitteilen, dass wir beabsichtigen, nur einige Dokumentseiten zu drucken.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft "FromPage" auf "1" und die Eigenschaft "ToPage" auf "3", um die Seiten 1 bis 3 zu drucken.
// Seitenindizierung ist 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument zu drucken.
// 1 - Drucken, während unsere Druckeinstellungen angewendet werden:
doc.Print(printerSettings);

// 2 - Drucken, während unsere Druckeinstellungen angewendet werden, während auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir in der Druckerwarteschlange erkennen können:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
