---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor XpsSaveOptions para crear sin esfuerzo instancias para guardar documentos en formato XPS, mejorando la eficiencia de la gestión de documentos.
type: docs
weight: 10
url: /es/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elXps formato.

```csharp
public XpsSaveOptions()
```

## Ejemplos

Muestra cómo limitar el nivel de encabezados que aparecerán en el esquema de un documento XPS guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas de TOC de los niveles 1, 2 y luego 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un objeto "XpsSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// El documento XPS de salida contendrá un esquema, una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir del esquema todos los encabezados cuyos niveles sean superiores a 2.
//Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ver también

* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elXps oOpenXps formato.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Ejemplos

Muestra cómo guardar un documento en formato XPS en forma de libro plegable.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "XpsSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Establezca la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en la salida XPS de una manera que nos ayuda a usarlo para hacer un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" en "false" para representar el XPS normalmente.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Si estamos renderizando el documento como un folleto, debemos configurar "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

//Una vez que imprimimos este documento, podemos convertirlo en un folleto apilando las páginas
// para salir de la impresora y doblar por la mitad.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
