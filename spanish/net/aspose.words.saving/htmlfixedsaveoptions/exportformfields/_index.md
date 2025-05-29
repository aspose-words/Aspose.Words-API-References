---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlFixedSaveOptions ExportFormFields mejora las exportaciones de sus documentos al mantener los campos de formulario interactivos y mejorando la experiencia del usuario.
type: docs
weight: 80
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Obtiene o establece la indicación de si los campos de formulario se exportan como elementos interactivos (como etiqueta 'input') en lugar de convertirse en texto o gráficos.

```csharp
public bool ExportFormFields { get; set; }
```

## Ejemplos

Muestra cómo exportar campos de formulario a HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Cuando exportamos un documento con campos de formulario a .html,
// Hay dos formas en que Aspose.Words puede exportar campos de formulario.
// Si establece el indicador "ExportFormFields" en "verdadero", los exportará como objetos interactivos.
// Si se establece esta bandera en "falso" los campos del formulario se mostrarán como texto simple.
// Esto los congelará en su valor actual y evitará que el lector de nuestro documento HTML
// de poder interactuar con ellos.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
