---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words per .NET
description: Document Print metodo. Stampa lintero documento sulla stampante predefinita in C#.
type: docs
weight: 640
url: /it/net/aspose.words/document/print/
---
## Print() {#print}

Stampa l'intero documento sulla stampante predefinita.

```csharp
public void Print()
```

## Esempi

Mostra come stampare un documento utilizzando la stampante predefinita.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Di seguito sono riportati due modi per stampare il nostro documento.
// 1 - Stampa utilizzando la stampante predefinita:
doc.Print();

// 2 - Specificare per nome la stampante con cui desideriamo stampare il documento:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Stampa l'intero documento sulla stampante specificata, utilizzando il controller di stampa standard (senza interfaccia utente).

```csharp
public void Print(string printerName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| printerName | String | Il nome della stampante. |

## Esempi

Mostra come stampare un documento utilizzando la stampante predefinita.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Di seguito sono riportati due modi per stampare il nostro documento.
// 1 - Stampa utilizzando la stampante predefinita:
doc.Print();

// 2 - Specificare per nome la stampante con cui desideriamo stampare il documento:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Stampa il documento in base alle impostazioni della stampante specificate, utilizzando il controller di stampa standard (senza interfaccia utente).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| printerSettings | PrinterSettings | Le impostazioni della stampante da utilizzare. |

## Osservazioni

ILPrinterSettings L'oggetto consente di specificare la stampante su cui stampare, l'intervallo di pagine da stampare e altre opzioni.

## Esempi

Mostra come stampare un intervallo di pagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un oggetto "PrinterSettings" per modificare il modo in cui stampiamo il documento.
PrinterSettings printerSettings = new PrinterSettings();

// Imposta la proprietà "PrintRange" su "PrintRange.SomePages" su
// comunica alla stampante che intendiamo stampare solo alcune pagine del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Imposta la proprietà "FromPage" su "1" e la proprietà "ToPage" su "3" per stampare le pagine da 1 a 3.
// L'indicizzazione della pagina è in base 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Di seguito sono riportati due modi per stampare il nostro documento.
// 1 - Stampa applicando le nostre impostazioni di stampa:
doc.Print(printerSettings);

// 2 - Stampa applicando le nostre impostazioni di stampa, while also
// dando al documento un nome personalizzato che potremmo riconoscere nella coda della stampante:
doc.Print(printerSettings, "My rendered document");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Stampa il documento in base alle impostazioni della stampante specificate, utilizzando il controller di stampa standard (senza interfaccia utente) e un nome documento.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| printerSettings | PrinterSettings | Le impostazioni della stampante da utilizzare. |
| documentName | String | Il nome del documento da visualizzare (ad esempio, in una finestra di dialogo di stato della stampa o nella coda della stampante) durante la stampa del documento. |

## Osservazioni

ILPrinterSettings L'oggetto consente di specificare la stampante su cui stampare, l'intervallo di pagine da stampare e altre opzioni.

## Esempi

Mostra come stampare un intervallo di pagine.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un oggetto "PrinterSettings" per modificare il modo in cui stampiamo il documento.
PrinterSettings printerSettings = new PrinterSettings();

// Imposta la proprietà "PrintRange" su "PrintRange.SomePages" su
// comunica alla stampante che intendiamo stampare solo alcune pagine del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Imposta la proprietà "FromPage" su "1" e la proprietà "ToPage" su "3" per stampare le pagine da 1 a 3.
// L'indicizzazione della pagina è in base 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Di seguito sono riportati due modi per stampare il nostro documento.
// 1 - Stampa applicando le nostre impostazioni di stampa:
doc.Print(printerSettings);

// 2 - Stampa applicando le nostre impostazioni di stampa, while also
// dando al documento un nome personalizzato che potremmo riconoscere nella coda della stampante:
doc.Print(printerSettings, "My rendered document");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
