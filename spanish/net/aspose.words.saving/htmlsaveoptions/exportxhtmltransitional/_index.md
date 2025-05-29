---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words para .NET
description: Optimice su HTML con la propiedad HtmlSaveOptions ExportXhtmlTransitional. Controle las declaraciones DOCTYPE para una mejor compatibilidad con los formatos HTML, MHTML y EPUB.
type: docs
weight: 280
url: /es/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Especifica si se debe escribir la declaración DOCTYPE al guardar en HTML o MHTML. Cuando`verdadero` , escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es`FALSO`. Al guardar en EPUB o HTML5 (Html5 ) la declaración DOCTYPE siempre se escribe.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Observaciones

Aspose.Words siempre escribe HTML bien formado independientemente de esta configuración.

Cuando`verdadero`, el comienzo del documento de salida HTML se verá así:

Aspose.Words busca generar XHTML según la especificación XHTML 1.0 Transitional, pero la salida no siempre se valida con el DTD. Algunas estructuras dentro de un documento de Microsoft Word son difíciles o imposibles de asignar a un documento que se valide con el esquema XHTML. Por ejemplo, XHTML no permite listas anidadas (una UL no puede anidarse dentro de otro elemento UL), pero en documentos de Microsoft Word las listas multinivel son bastante frecuentes.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transicional//ES"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="es" lang="es">
```

## Ejemplos

Muestra cómo mostrar un encabezado DOCTYPE al convertir documentos al estándar de transición Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Nuestro documento solo contendrá un encabezado de declaración DOCTYPE si hemos establecido el indicador "ExportXhtmlTransitional" en "verdadero".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//ES\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
