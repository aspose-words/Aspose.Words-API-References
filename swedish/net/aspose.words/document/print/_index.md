---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words för .NET
description: Skriv enkelt ut hela ditt dokument till din standardskrivare med vår effektiva dokumentutskriftsmetod. Njut av snabb och problemfri utskrift!
type: docs
weight: 680
url: /sv/net/aspose.words/document/print/
---
## Print() {#print}

Skriver ut hela dokumentet till standardskrivaren.

```csharp
public void Print()
```

## Exempel

Visar hur man skriver ut ett dokument med standardskrivaren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nedan följer två sätt att skriva ut vårt dokument.
// 1 - Skriv ut med standardskrivaren:
doc.Print();

// 2 - Ange en skrivare som vi vill skriva ut dokumentet med, med namn:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Skriv ut hela dokumentet till den angivna skrivaren, med hjälp av standardutskriftskontrollen (inget användargränssnitt).

```csharp
public void Print(string printerName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| printerName | String | Skrivarens namn. |

## Exempel

Visar hur man skriver ut ett dokument med standardskrivaren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Nedan följer två sätt att skriva ut vårt dokument.
// 1 - Skriv ut med standardskrivaren:
doc.Print();

// 2 - Ange en skrivare som vi vill skriva ut dokumentet med, med namn:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Skriver ut dokumentet enligt de angivna skrivarinställningarna, med hjälp av standardutskriftskontrollen (inget användargränssnitt).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| printerSettings | PrinterSettings | Skrivarinställningarna som ska användas. |

## Anmärkningar

DePrinterSettings Med objektet kan du ange vilken skrivare som ska skrivas ut på, sidintervallet som ska skrivas ut och andra alternativ.

## Exempel

Visar hur man skriver ut ett sidintervall.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "PrinterSettings"-objekt för att ändra hur vi skriver ut dokumentet.
PrinterSettings printerSettings = new PrinterSettings();

// Ställ in egenskapen "PrintRange" till "PrintRange.SomePages" för att
// berätta för skrivaren att vi bara avser att skriva ut vissa dokumentsidor.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Sätt egenskapen "FromPage" till "1" och egenskapen "ToPage" till "3" för att skriva ut sidorna 1 till 3.
// Sidindexering är 1-baserad.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nedan följer två sätt att skriva ut vårt dokument.
// 1 - Skriv ut medan våra utskriftsinställningar tillämpas:
doc.Print(printerSettings);

// 2 - Skriv ut medan du tillämpar våra utskriftsinställningar, samtidigt som du
// ger dokumentet ett anpassat namn som vi kan känna igen i skrivarkön:
doc.Print(printerSettings, "My rendered document");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Skriver ut dokumentet enligt de angivna skrivarinställningarna, med hjälp av standardutskriftskontrollen (inget användargränssnitt) och ett dokumentnamn.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| printerSettings | PrinterSettings | Skrivarinställningarna som ska användas. |
| documentName | String | Dokumentnamnet som ska visas (till exempel i en dialogruta för utskriftsstatus eller i skrivarkön) vid utskrift av dokumentet. |

## Anmärkningar

DePrinterSettings Med objektet kan du ange vilken skrivare som ska skrivas ut på, sidintervallet som ska skrivas ut och andra alternativ.

## Exempel

Visar hur man skriver ut ett sidintervall.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "PrinterSettings"-objekt för att ändra hur vi skriver ut dokumentet.
PrinterSettings printerSettings = new PrinterSettings();

// Ställ in egenskapen "PrintRange" till "PrintRange.SomePages" för att
// berätta för skrivaren att vi bara avser att skriva ut vissa dokumentsidor.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Sätt egenskapen "FromPage" till "1" och egenskapen "ToPage" till "3" för att skriva ut sidorna 1 till 3.
// Sidindexering är 1-baserad.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Nedan följer två sätt att skriva ut vårt dokument.
// 1 - Skriv ut medan våra utskriftsinställningar tillämpas:
doc.Print(printerSettings);

// 2 - Skriv ut medan du tillämpar våra utskriftsinställningar, samtidigt som du
// ger dokumentet ett anpassat namn som vi kan känna igen i skrivarkön:
doc.Print(printerSettings, "My rendered document");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
