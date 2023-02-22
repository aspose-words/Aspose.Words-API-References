---
title: Document.Print
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Imprime todo el documento en la impresora predeterminada.
type: docs
weight: 620
url: /es/net/aspose.words/document/print/
---
## Print() {#print}

Imprime todo el documento en la impresora predeterminada.

```csharp
public void Print()
```

### Ejemplos

Muestra cómo imprimir un documento utilizando la impresora predeterminada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir usando la impresora predeterminada:
doc.Print();

// 2 - Especificar una impresora con la que deseamos imprimir el documento por nombre:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Print(string) {#print_3}

Imprima todo el documento en la impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario).

```csharp
public void Print(string printerName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerName | String | El nombre de la impresora. |

### Ejemplos

Muestra cómo imprimir un documento utilizando la impresora predeterminada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprimir usando la impresora predeterminada:
doc.Print();

// 2 - Especificar una impresora con la que deseamos imprimir el documento por nombre:
string myPrinter = PrinterSettings.InstalledPrinters[4];

Assert.AreEqual("HPDAAB96 (HP ENVY 5000 series)", myPrinter);

doc.Print(myPrinter);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Print(PrinterSettings) {#print_1}

Imprime el documento de acuerdo con la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario).

```csharp
public void Print(PrinterSettings printerSettings)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerSettings | PrinterSettings | La configuración de la impresora a utilizar. |

### Observaciones

losPrinterSettings El objeto le permite especificar la impresora para imprimir, el rango de páginas para imprimir y otras opciones.

### Ejemplos

Muestra cómo imprimir un rango de páginas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crear un objeto "PrinterSettings" para modificar cómo imprimimos el documento.
PrinterSettings printerSettings = new PrinterSettings();

// Establecer la propiedad "PrintRange" en "PrintRange.SomePages" para
// decirle a la impresora que pretendemos imprimir solo algunas páginas del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Establezca la propiedad "FromPage" en "1" y la propiedad "ToPage" en "3" para imprimir las páginas 1 a 3.
// La indexación de páginas se basa en 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprime mientras aplicas nuestra configuración de impresión:
doc.Print(printerSettings);

// 2 - Imprima mientras aplica nuestra configuración de impresión, mientras también
// dando al documento un nombre personalizado que podamos reconocer en la cola de la impresora:
doc.Print(printerSettings, "My rendered document");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Print(PrinterSettings, string) {#print_2}

Imprime el documento de acuerdo con la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario) y un nombre de documento.

```csharp
public void Print(PrinterSettings printerSettings, string documentName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| printerSettings | PrinterSettings | La configuración de la impresora a utilizar. |
| documentName | String | El nombre del documento que se mostrará (por ejemplo, en un cuadro de diálogo de estado de impresión o en la cola de la impresora) mientras se imprime el documento. |

### Observaciones

losPrinterSettings El objeto le permite especificar la impresora para imprimir, el rango de páginas para imprimir y otras opciones.

### Ejemplos

Muestra cómo imprimir un rango de páginas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crear un objeto "PrinterSettings" para modificar cómo imprimimos el documento.
PrinterSettings printerSettings = new PrinterSettings();

// Establecer la propiedad "PrintRange" en "PrintRange.SomePages" para
// decirle a la impresora que pretendemos imprimir solo algunas páginas del documento.
printerSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;

// Establezca la propiedad "FromPage" en "1" y la propiedad "ToPage" en "3" para imprimir las páginas 1 a 3.
// La indexación de páginas se basa en 1.
printerSettings.FromPage = 1;
printerSettings.ToPage = 3;

// A continuación se muestran dos formas de imprimir nuestro documento.
// 1 - Imprime mientras aplicas nuestra configuración de impresión:
doc.Print(printerSettings);

// 2 - Imprima mientras aplica nuestra configuración de impresión, mientras también
// dando al documento un nombre personalizado que podamos reconocer en la cola de la impresora:
doc.Print(printerSettings, "My rendered document");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


