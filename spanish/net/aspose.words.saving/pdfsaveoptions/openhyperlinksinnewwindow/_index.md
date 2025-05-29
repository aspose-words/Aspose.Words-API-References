---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words para .NET
description: Controle el comportamiento de los hipervínculos en su PDF con PdfSaveOptions. Configure fácilmente los enlaces para que se abran en una nueva ventana o pestaña para una mejor experiencia de usuario.
type: docs
weight: 230
url: /es/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Obtiene o establece un valor que determina si los hipervínculos en el documento Pdf de salida se fuerzan a abrirse en una nueva ventana (o pestaña) de un navegador.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` . Cuando este valor se establece en`verdadero` Los hipervínculos se guardan mediante código JavaScript. El código JavaScript es`aplicación.launchURL("URL", verdadero);` , donde`URL` es un hipervínculo.

Tenga en cuenta que si esta opción está configurada en`verdadero` Los hipervínculos no pueden funcionar en algunos lectores de PDF, por ejemplo, Chrome y Firefox.

Las acciones de JavaScript están prohibidas por la conformidad con PDF/A-1 y PDF/A-2.`FALSO`Se utilizará automáticamente cuando se guarde en PDF/A-1 y PDF/A-2.

## Ejemplos

Muestra cómo guardar hipervínculos en un documento que convertimos a PDF para que abran nuevas páginas cuando hagamos clic en ellos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", falso);

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "OpenHyperlinksInNewWindow" en "verdadero" para guardar todos los hipervínculos mediante código Javascript
// que obliga a los lectores a abrir estos enlaces en nuevas ventanas o pestañas del navegador.
// Establezca la propiedad "OpenHyperlinksInNewWindow" en "false" para guardar todos los hipervínculos normalmente.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
