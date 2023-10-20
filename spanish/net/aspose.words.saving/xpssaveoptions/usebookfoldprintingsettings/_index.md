---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words para .NET
description: XpsSaveOptions UseBookFoldPrintingSettings propiedad. Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión de folleto si se especifica medianteMultiplePages  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset/) se ignora al guardar. Este comportamiento coincide con MS Word. Si la configuración de impresión de plegado de libro no se especifica en la configuración de página, esta opción no tendrá ningún efecto.

## Ejemplos

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

* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
