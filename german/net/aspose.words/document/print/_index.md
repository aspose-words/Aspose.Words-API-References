---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words für .NET
description: Drucken Sie Ihr gesamtes Dokument mühelos auf Ihrem Standarddrucker mit unserer optimierten Dokumentendruckmethode. Genießen Sie schnelles und problemloses Drucken!
type: docs
weight: 680
url: /de/net/aspose.words/document/print/
---
## Print() {#print}

Druckt das gesamte Dokument auf dem Standarddrucker.

```csharp
public void Print()
```

## Beispiele

Zeigt, wie ein Dokument mit dem Standarddrucker gedruckt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Unten sind zwei Möglichkeiten zum Drucken unseres Dokuments aufgeführt.
// 1 - Drucken mit dem Standarddrucker:
doc.Print();

// 2 - Geben Sie den Namen eines Druckers an, mit dem wir das Dokument drucken möchten:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Drucken Sie das gesamte Dokument auf dem angegebenen Drucker, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche).

```csharp
public void Print(string printerName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerName | String | Der Name des Druckers. |

## Beispiele

Zeigt, wie ein Dokument mit dem Standarddrucker gedruckt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Unten sind zwei Möglichkeiten zum Drucken unseres Dokuments aufgeführt.
// 1 - Drucken mit dem Standarddrucker:
doc.Print();

// 2 - Geben Sie den Namen eines Druckers an, mit dem wir das Dokument drucken möchten:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Druckt das Dokument gemäß den angegebenen Druckereinstellungen unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |

## Bemerkungen

DerPrinterSettings Mit dem Objekt können Sie den Drucker, auf dem gedruckt werden soll, den zu druckenden Seitenbereich und andere Optionen angeben.

## Beispiele

Zeigt, wie ein Seitenbereich gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „PrinterSettings“-Objekt, um die Art und Weise zu ändern, wie das Dokument gedruckt wird.
PrinterSettings printerSettings = new PrinterSettings();

// Setzen Sie die Eigenschaft "PrintRange" auf "PrintRange.SomePages" auf
// dem Drucker mitteilen, dass wir nur einige Dokumentseiten drucken möchten.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft „FromPage“ auf „1“ und die Eigenschaft „ToPage“ auf „3“, um die Seiten 1 bis 3 zu drucken.
// Die Seitenindizierung ist 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Unten sind zwei Möglichkeiten zum Drucken unseres Dokuments aufgeführt.
// 1 - Drucken, während unsere Druckeinstellungen angewendet werden:
doc.Print(printerSettings);

// 2 - Drucken Sie, während Sie unsere Druckeinstellungen anwenden, während Sie auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir in der Druckerwarteschlange wiedererkennen können:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Druckt das Dokument entsprechend den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (ohne Benutzeroberfläche) und eines Dokumentnamens.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |
| documentName | String | Der beim Drucken des Dokuments anzuzeigende Dokumentname (z. B. in einem Druckstatusdialogfeld oder einer Druckerwarteschlange). |

## Bemerkungen

DerPrinterSettings Mit dem Objekt können Sie den Drucker, auf dem gedruckt werden soll, den zu druckenden Seitenbereich und andere Optionen angeben.

## Beispiele

Zeigt, wie ein Seitenbereich gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „PrinterSettings“-Objekt, um die Art und Weise zu ändern, wie das Dokument gedruckt wird.
PrinterSettings printerSettings = new PrinterSettings();

// Setzen Sie die Eigenschaft "PrintRange" auf "PrintRange.SomePages" auf
// dem Drucker mitteilen, dass wir nur einige Dokumentseiten drucken möchten.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft „FromPage“ auf „1“ und die Eigenschaft „ToPage“ auf „3“, um die Seiten 1 bis 3 zu drucken.
// Die Seitenindizierung ist 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Unten sind zwei Möglichkeiten zum Drucken unseres Dokuments aufgeführt.
// 1 - Drucken, während unsere Druckeinstellungen angewendet werden:
doc.Print(printerSettings);

// 2 - Drucken Sie, während Sie unsere Druckeinstellungen anwenden, während Sie auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir in der Druckerwarteschlange wiedererkennen können:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
