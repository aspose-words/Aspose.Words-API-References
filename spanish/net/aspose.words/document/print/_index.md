---
title: Document.Print
linktitle: Print
articleTitle: Print
second_title: Aspose.Words para .NET
description: Imprima fácilmente todo su documento en su impresora predeterminada con nuestro método optimizado de Impresión de Documentos. ¡Disfrute de una impresión rápida y sin complicaciones!
type: docs
weight: 680
url: /es/net/aspose.words/document/print/
---
## Print() {#print}

Imprime todo el documento en la impresora predeterminada.

```csharp
public void Print()
```

## Ejemplos

Muestra cómo imprimir un documento utilizando la impresora predeterminada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

//A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir utilizando la impresora predeterminada:
doc.Print();

// 2 - Especificamos una impresora con la que deseamos imprimir el documento por nombre:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Print(*string*) {#print_3}

Imprimir todo el documento en la impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario).

```csharp
public void Print(string printerName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerName | String | El nombre de la impresora. |

## Ejemplos

Muestra cómo imprimir un documento utilizando la impresora predeterminada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

//A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir utilizando la impresora predeterminada:
doc.Print();

// 2 - Especificamos una impresora con la que deseamos imprimir el documento por nombre:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Print(*PrinterSettings*) {#print_1}

Imprime el documento según la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerSettings | PrinterSettings | La configuración de impresora a utilizar. |

## Observaciones

ElPrinterSettings El objeto le permite especificar la impresora en la que imprimir, el rango de páginas a imprimir y otras opciones.

## Ejemplos

Muestra cómo imprimir un rango de páginas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "PrinterSettings" para modificar cómo imprimimos el documento.
PrinterSettings printerSettings = new PrinterSettings();

// Establezca la propiedad "PrintRange" en "PrintRange.SomePages" para
// Le decimos a la impresora que queremos imprimir sólo algunas páginas del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Establezca la propiedad "FromPage" en "1" y la propiedad "ToPage" en "3" para imprimir las páginas 1 a 3.
// La indexación de páginas se basa en 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

//A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir mientras aplicamos nuestra configuración de impresión:
doc.Print(printerSettings);

// 2 - Imprimir mientras aplicamos nuestra configuración de impresión, mientras también
// dándole al documento un nombre personalizado que podamos reconocer en la cola de impresión:
doc.Print(printerSettings, "My rendered document");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Print(*PrinterSettings, string*) {#print_2}

Imprime el documento según la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario) y un nombre de documento.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerSettings | PrinterSettings | La configuración de impresora a utilizar. |
| documentName | String | El nombre del documento que se mostrará (por ejemplo, en un cuadro de diálogo de estado de impresión o en la cola de impresión) mientras se imprime el documento. |

## Observaciones

ElPrinterSettings El objeto le permite especificar la impresora en la que imprimir, el rango de páginas a imprimir y otras opciones.

## Ejemplos

Muestra cómo imprimir un rango de páginas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "PrinterSettings" para modificar cómo imprimimos el documento.
PrinterSettings printerSettings = new PrinterSettings();

// Establezca la propiedad "PrintRange" en "PrintRange.SomePages" para
// Le decimos a la impresora que queremos imprimir sólo algunas páginas del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Establezca la propiedad "FromPage" en "1" y la propiedad "ToPage" en "3" para imprimir las páginas 1 a 3.
// La indexación de páginas se basa en 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

//A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir mientras aplicamos nuestra configuración de impresión:
doc.Print(printerSettings);

// 2 - Imprimir mientras aplicamos nuestra configuración de impresión, mientras también
// dándole al documento un nombre personalizado que podamos reconocer en la cola de impresión:
doc.Print(printerSettings, "My rendered document");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
