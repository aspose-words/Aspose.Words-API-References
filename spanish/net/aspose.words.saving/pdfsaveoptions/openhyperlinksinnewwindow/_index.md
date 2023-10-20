---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words para .NET
description: PdfSaveOptions OpenHyperlinksInNewWindow propiedad. Obtiene o establece un valor que determina si los hipervínculos en el documento PDF de salida se fuerzan a abrirse en una nueva ventana o pestaña de un navegador en C#.
type: docs
weight: 230
url: /es/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Obtiene o establece un valor que determina si los hipervínculos en el documento PDF de salida se fuerzan a abrirse en una nueva ventana (o pestaña) de un navegador.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` . Cuando este valor se establece en`verdadero` los hipervínculos se guardan usando código JavaScript. El código JavaScript es`app.launchURL("URL", verdadero);` , donde`URL` es un hipervínculo.

Tenga en cuenta que si esta opción está configurada en`verdadero` los hipervínculos no pueden funcionar en algunos lectores de PDF, por ejemplo, Chrome, Firefox.

Las acciones de JavaScript están prohibidas por el cumplimiento de PDF/A-1 y PDF/A-2.`FALSO`se utilizará automáticamente cuando guarde en PDF/A-1 y PDF/A-2.

## Ejemplos

Muestra cómo guardar hipervínculos en un documento que convertimos a PDF para que abran nuevas páginas cuando hagamos clic en ellos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "OpenHyperlinksInNewWindow" en "true" para guardar todos los hipervínculos usando código Javascript
// que obliga a los lectores a abrir estos enlaces en nuevas ventanas/pestañas del navegador.
// Establece la propiedad "OpenHyperlinksInNewWindow" en "false" para guardar todos los hipervínculos normalmente.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
