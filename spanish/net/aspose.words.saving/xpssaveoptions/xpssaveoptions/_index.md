---
title: XpsSaveOptions.XpsSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: XpsSaveOptions constructor. Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elXps formato.
type: docs
weight: 10
url: /es/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elXps formato.

```csharp
public XpsSaveOptions()
```

### Ejemplos

Muestra cómo limitar el nivel de los encabezados que aparecerán en el esquema de un documento XPS guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas TOC de los niveles 1, 2 y luego 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un objeto "XpsSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// El documento XPS de salida contendrá un esquema, una tabla de contenido que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "2" para excluir del esquema todos los encabezados cuyos niveles estén por encima de 2.
// Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ver también

* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../xpssaveoptions/)
* asamblea [Aspose.Words](../../../)

---

## XpsSaveOptions(SaveFormat) {#constructor_1}

Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elXps oOpenXps formato.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

### Ejemplos

Muestra cómo guardar un documento en formato XPS en forma de libro plegado.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "XpsSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Establece la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en el XPS de salida de una manera que nos ayude a usarlo para hacer un folleto.
// Establece la propiedad "UseBookFoldPrintingSettings" en "false" para representar el XPS normalmente.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Si renderizamos el documento como un folleto, debemos configurar "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones en "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una vez que imprimamos este documento, podemos convertirlo en un folleto apilando las páginas
// para salir de la impresora y doblar por la mitad.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../xpssaveoptions/)
* asamblea [Aspose.Words](../../../)


