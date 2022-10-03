---
title: Print
second_title: Référence de l'API Aspose.Words pour .NET
description: Imprime tout le document sur limprimante par défaut.
type: docs
weight: 620
url: /fr/net/aspose.words/document/print/
---
## Print() {#print}

Imprime tout le document sur l'imprimante par défaut.

```csharp
public void Print()
```

### Exemples

Montre comment imprimer un document à l'aide de l'imprimante par défaut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en utilisant l'imprimante par défaut :
doc.Print();

// 2 - Spécifiez une imprimante avec laquelle nous souhaitons imprimer le document par son nom :
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Imprimez l'intégralité du document sur l'imprimante spécifiée, à l'aide du contrôleur d'impression standard (sans interface utilisateur).

```csharp
public void Print(string printerName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerName | String | Le nom de l'imprimante. |

### Exemples

Montre comment imprimer un document à l'aide de l'imprimante par défaut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en utilisant l'imprimante par défaut :
doc.Print();

// 2 - Spécifiez une imprimante avec laquelle nous souhaitons imprimer le document par son nom :
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Imprime le document conformément aux paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (pas d'interface utilisateur).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerSettings | PrinterSettings | Les paramètres de l'imprimante à utiliser. |

### Remarques

LaPrinterSettings L'objet vous permet de spécifier l'imprimante sur laquelle imprimer, la plage de pages à imprimer et d'autres options.

### Exemples

Montre comment imprimer une plage de pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crée un objet "PrinterSettings" pour modifier la façon dont nous imprimons le document.
PrinterSettings printerSettings = new PrinterSettings();

// Définissez la propriété "PrintRange" sur "PrintRange.SomePages" pour
// indique à l'imprimante que nous avons l'intention d'imprimer uniquement certaines pages du document.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Définissez la propriété "FromPage" sur "1" et la propriété "ToPage" sur "3" pour imprimer les pages 1 à 3.
// L'indexation des pages est basée sur 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en appliquant nos paramètres d'impression :
doc.Print(printerSettings);

// 2 - Imprimer en appliquant nos paramètres d'impression, tout en
// donnant au document un nom personnalisé que nous pouvons reconnaître dans la file d'attente de l'imprimante :
doc.Print(printerSettings, "My rendered document");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Imprime le document conformément aux paramètres d'imprimante spécifiés, à l'aide du contrôleur d'impression standard (pas d'interface utilisateur) et d'un nom de document.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| printerSettings | PrinterSettings | Les paramètres de l'imprimante à utiliser. |
| documentName | String | Nom du document à afficher (par exemple, dans une boîte de dialogue d'état d'impression ou une file d'attente d'impression) lors de l'impression du document. |

### Remarques

LaPrinterSettings L'objet vous permet de spécifier l'imprimante sur laquelle imprimer, la plage de pages à imprimer et d'autres options.

### Exemples

Montre comment imprimer une plage de pages.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crée un objet "PrinterSettings" pour modifier la façon dont nous imprimons le document.
PrinterSettings printerSettings = new PrinterSettings();

// Définissez la propriété "PrintRange" sur "PrintRange.SomePages" pour
// indique à l'imprimante que nous avons l'intention d'imprimer uniquement certaines pages du document.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Définissez la propriété "FromPage" sur "1" et la propriété "ToPage" sur "3" pour imprimer les pages 1 à 3.
// L'indexation des pages est basée sur 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// Vous trouverez ci-dessous deux manières d'imprimer notre document.
// 1 - Imprimer en appliquant nos paramètres d'impression :
doc.Print(printerSettings);

// 2 - Imprimer en appliquant nos paramètres d'impression, tout en
// donnant au document un nom personnalisé que nous pouvons reconnaître dans la file d'attente de l'imprimante :
doc.Print(printerSettings, "My rendered document");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
