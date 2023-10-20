---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words para .NET
description: HtmlSaveOptions ExportXhtmlTransitional propiedad. Especifica si se escribe la declaración DOCTYPE al guardar en HTML o MHTML. Cuandoverdadero  escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado esFALSO. Al guardar en EPUB o HTML5 Html5  la declaración DOCTYPE siempre se escribe en C#.
type: docs
weight: 280
url: /es/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Especifica si se escribe la declaración DOCTYPE al guardar en HTML o MHTML. Cuando`verdadero` , escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es`FALSO`. Al guardar en EPUB o HTML5 (Html5 ) la declaración DOCTYPE siempre se escribe.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Observaciones

Aspose.Words siempre escribe HTML bien formado independientemente de esta configuración.

Cuando`verdadero`, el comienzo del documento de salida HTML se verá así:

Aspose.Words tiene como objetivo generar XHTML de acuerdo con la especificación transitoria XHTML 1.0, , pero la salida no siempre se validará con la DTD. Algunas estructuras dentro de un documento de Microsoft Word son difíciles o imposibles de asignar a un documento que se validará con el esquema XHTML. Por ejemplo, XHTML no permite listas anidadas (UL no se puede anidar dentro de otro elemento UL), pero en documentos de Microsoft Word las listas multinivel ocurren con bastante frecuencia.

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

// Nuestro documento sólo contendrá un encabezado de declaración DOCTYPE si hemos configurado el indicador "ExportXhtmlTransitional" en "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transicional//ES\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
