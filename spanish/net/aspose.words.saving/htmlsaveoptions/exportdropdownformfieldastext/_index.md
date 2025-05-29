---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ExportDropDownFormFieldAsText mejora sus exportaciones HTML/MHTML controlando los formatos de los campos desplegables. ¡Optimice sus documentos!
type: docs
weight: 130
url: /es/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Controla cómo se guardan los campos del formulario desplegable en HTML o MHTML. El valor predeterminado es`FALSO` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Observaciones

Cuando se establece en`verdadero` , exporta campos de formulario desplegable como texto normal. Cuando`FALSO`, exporta campos de formulario desplegable como elemento SELECT en HTML.

Al exportar a EPUB, los campos de formulario desplegable de texto siempre se guardan como texto debido a los requisitos de este formato.

## Ejemplos

Muestra cómo lograr que los campos de formulario del cuadro combinado desplegable se combinen con el texto del párrafo al guardar en HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilice un generador de documentos para insertar un cuadro combinado con el valor "Dos" seleccionado.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// El indicador "ExportDropDownFormFieldAsText" de este objeto SaveOptions nos permite
// controla cómo se tratan los cuadros combinados desplegables al guardar el documento en HTML.
// Establecerlo como "verdadero" convertirá cada cuadro combinado en texto simple
// que muestra el valor seleccionado actualmente del cuadro combinado, congelándolo efectivamente.
// Establecerlo como "falso" preservará la funcionalidad del cuadro combinado usando las etiquetas <select> y <option>.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
