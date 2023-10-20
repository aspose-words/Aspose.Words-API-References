---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words für .NET
description: Document Print methode. Druckt das gesamte Dokument auf dem Standarddrucker in C#.
type: docs
weight: 640
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

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument auszudrucken.
// 1 – Drucken mit dem Standarddrucker:
doc.Print();

// 2 – Geben Sie den Namen eines Druckers an, mit dem wir das Dokument drucken möchten:
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

Drucken Sie das gesamte Dokument auf dem angegebenen Drucker. Verwenden Sie den Standard-Druckcontroller (keine Benutzeroberfläche).

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

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument auszudrucken.
// 1 – Drucken mit dem Standarddrucker:
doc.Print();

// 2 – Geben Sie den Namen eines Druckers an, mit dem wir das Dokument drucken möchten:
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

Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (keine Benutzeroberfläche).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |

## Bemerkungen

DerPrinterSettings Mit dem -Objekt können Sie den Drucker, auf dem gedruckt werden soll, den zu druckenden Seitenbereich und andere Optionen angeben.

## Beispiele

Zeigt, wie mehrere Seiten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „PrinterSettings“-Objekt, um zu ändern, wie wir das Dokument drucken.
PrinterSettings printerSettings = new PrinterSettings();

// Setzen Sie die Eigenschaft „PrintRange“ auf „PrintRange.SomePages“.
// Teilen Sie dem Drucker mit, dass wir nur einige Dokumentseiten drucken möchten.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft „FromPage“ auf „1“ und die Eigenschaft „ToPage“ auf „3“, um die Seiten 1 bis 3 zu drucken.
// Die Seitenindizierung erfolgt 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument auszudrucken.
// 1 – Drucken unter Anwendung unserer Druckeinstellungen:
doc.Print(printerSettings);

// 2 – Drucken, während unsere Druckeinstellungen angewendet werden, während auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir möglicherweise in der Druckerwarteschlange erkennen:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (keine Benutzeroberfläche) und eines Dokumentnamens.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| printerSettings | PrinterSettings | Die zu verwendenden Druckereinstellungen. |
| documentName | String | Der Name des Dokuments, das beim Drucken des Dokuments angezeigt werden soll (z. B. in einem Feld „Druckstatus“ oder in einer Druckerwarteschlange). |

## Bemerkungen

DerPrinterSettings Mit dem -Objekt können Sie den Drucker, auf dem gedruckt werden soll, den zu druckenden Seitenbereich und andere Optionen angeben.

## Beispiele

Zeigt, wie mehrere Seiten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Erstellen Sie ein „PrinterSettings“-Objekt, um zu ändern, wie wir das Dokument drucken.
PrinterSettings printerSettings = new PrinterSettings();

// Setzen Sie die Eigenschaft „PrintRange“ auf „PrintRange.SomePages“.
// Teilen Sie dem Drucker mit, dass wir nur einige Dokumentseiten drucken möchten.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Setzen Sie die Eigenschaft „FromPage“ auf „1“ und die Eigenschaft „ToPage“ auf „3“, um die Seiten 1 bis 3 zu drucken.
// Die Seitenindizierung erfolgt 1-basiert.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nachfolgend finden Sie zwei Möglichkeiten, unser Dokument auszudrucken.
// 1 – Drucken unter Anwendung unserer Druckeinstellungen:
doc.Print(printerSettings);

// 2 – Drucken, während unsere Druckeinstellungen angewendet werden, während auch
// Geben Sie dem Dokument einen benutzerdefinierten Namen, den wir möglicherweise in der Druckerwarteschlange erkennen:
doc.Print(printerSettings, "My rendered document");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
