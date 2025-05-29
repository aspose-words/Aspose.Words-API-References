---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words pour .NET
description: Imprimez facilement l'intégralité de votre document sur votre imprimante par défaut grâce à notre méthode d'impression simplifiée. Profitez d'une impression rapide et sans tracas !
type: docs
weight: 680
url: /fr/net/aspose.words/document/print/
---
## Print() {#print}

Imprime l'intégralité du document sur l'imprimante par défaut.

```csharp
public void Print()
```

## Exemples

Montre comment imprimer un document à l’aide de l’imprimante par défaut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en utilisant l'imprimante par défaut :
doc.Print();

// 2 - Spécifiez une imprimante avec laquelle nous souhaitons imprimer le document par son nom :
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Imprimez l'intégralité du document sur l'imprimante spécifiée, à l'aide du contrôleur d'impression standard (sans interface utilisateur).

```csharp
public void Print(string printerName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerName | String | Le nom de l'imprimante. |

## Exemples

Montre comment imprimer un document à l’aide de l’imprimante par défaut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en utilisant l'imprimante par défaut :
doc.Print();

// 2 - Spécifiez une imprimante avec laquelle nous souhaitons imprimer le document par son nom :
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Imprime le document selon les paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (sans interface utilisateur).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerSettings | PrinterSettings | Les paramètres de l'imprimante à utiliser. |

## Remarques

LePrinterSettings L'objet vous permet de spécifier l'imprimante sur laquelle imprimer, la plage de pages à imprimer et d'autres options.

## Exemples

Montre comment imprimer une plage de pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Créez un objet « PrinterSettings » pour modifier la façon dont nous imprimons le document.
PrinterSettings printerSettings = new PrinterSettings();

// Définissez la propriété « PrintRange » sur « PrintRange.SomePages » pour
// indiquez à l'imprimante que nous avons l'intention d'imprimer uniquement certaines pages du document.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Définissez la propriété « FromPage » sur « 1 » et la propriété « ToPage » sur « 3 » pour imprimer les pages 1 à 3.
// L'indexation des pages est basée sur 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer tout en appliquant nos paramètres d'impression :
doc.Print(printerSettings);

// 2 - Imprimez tout en appliquant nos paramètres d'impression, tout en
// en donnant au document un nom personnalisé que nous pouvons reconnaître dans la file d'attente de l'imprimante :
doc.Print(printerSettings, "My rendered document");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Imprime le document selon les paramètres d'imprimante spécifiés, en utilisant le contrôleur d'impression standard (sans interface utilisateur) et un nom de document.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerSettings | PrinterSettings | Les paramètres de l'imprimante à utiliser. |
| documentName | String | Le nom du document à afficher (par exemple, dans une boîte de dialogue d'état d'impression ou dans une file d'attente d'impression) lors de l'impression du document. |

## Remarques

LePrinterSettings L'objet vous permet de spécifier l'imprimante sur laquelle imprimer, la plage de pages à imprimer et d'autres options.

## Exemples

Montre comment imprimer une plage de pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Créez un objet « PrinterSettings » pour modifier la façon dont nous imprimons le document.
PrinterSettings printerSettings = new PrinterSettings();

// Définissez la propriété « PrintRange » sur « PrintRange.SomePages » pour
// indiquez à l'imprimante que nous avons l'intention d'imprimer uniquement certaines pages du document.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Définissez la propriété « FromPage » sur « 1 » et la propriété « ToPage » sur « 3 » pour imprimer les pages 1 à 3.
// L'indexation des pages est basée sur 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer tout en appliquant nos paramètres d'impression :
doc.Print(printerSettings);

// 2 - Imprimez tout en appliquant nos paramètres d'impression, tout en
// en donnant au document un nom personnalisé que nous pouvons reconnaître dans la file d'attente de l'imprimante :
doc.Print(printerSettings, "My rendered document");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
