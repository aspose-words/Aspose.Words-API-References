---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: Descubra el método Clonar PdfSaveOptions para crear sin esfuerzo un clon profundo de sus objetos, mejorando sus capacidades de gestión de PDF.
type: docs
weight: 370
url: /es/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Crea un clon profundo de este objeto.

```csharp
public PdfSaveOptions Clone()
```

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

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
