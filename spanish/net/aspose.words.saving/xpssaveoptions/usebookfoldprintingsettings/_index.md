---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words para .NET
description: Optimice el diseño de su documento con la propiedad UseBookFoldPrintingSettings de XpsSaveOptions, que permite una impresión de folletos perfecta para una presentación mejorada.
type: docs
weight: 50
url: /es/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset/) Se ignora al guardar. Este comportamiento coincide con MS Word. Si no se especifican las configuraciones de impresión de plegado de libro en la configuración de página, esta opción no tendrá efecto.

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

* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
