---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SaveOptions UpdateFields optimiza el guardado de documentos actualizando tipos de campos específicos antes de convertirlos a formatos fijos. Valor predeterminado: verdadero.
type: docs
weight: 170
url: /es/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` .

```csharp
public bool UpdateFields { get; set; }
```

## Observaciones

Permite especificar si se debe imitar o no el comportamiento de MS Word.

## Ejemplos

Muestra cómo actualizar todos los campos de un documento inmediatamente antes de guardarlo en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Insertar texto con los campos PAGE y NUMPAGES. Estos campos no muestran el valor correcto en tiempo real.
// Necesitaremos actualizarlos manualmente utilizando métodos de actualización como "Field.Update()" y "Document.UpdateFields()"
// cada vez que necesitamos que muestren valores precisos.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "UpdateFields" en "falso" para no actualizar todos los campos de un documento justo antes de una operación de guardado.
// Esta es la opción preferible si sabemos que todos nuestros campos estarán actualizados antes de guardar.
// Establezca la propiedad "UpdateFields" en "verdadero" para iterar a través de todo el documento
// campos y actualizarlos antes de guardarlo como PDF. Esto garantizará que se muestren todos los campos.
// los valores más precisos en el PDF.
options.UpdateFields = updateFields;

//Podemos clonar objetos PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
