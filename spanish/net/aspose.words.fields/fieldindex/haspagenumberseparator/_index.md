---
title: FieldIndex.HasPageNumberSeparator
linktitle: HasPageNumberSeparator
articleTitle: HasPageNumberSeparator
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldIndex HasPageNumberSeparator, que revela si un separador de número de página está personalizado a través del código de campo para un formato mejorado del documento.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

Obtiene un valor que indica si se reemplaza un separador de número de página a través del código del campo.

```csharp
public bool HasPageNumberSeparator { get; }
```

## Ejemplos

Muestra cómo editar el separador de número de página en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX agrupará los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Si nuestro campo INDEX tiene una entrada para un grupo de campos XE,
// esta entrada mostrará el número de cada página que contiene un campo XE que pertenece a este grupo.
//Podemos configurar separadores personalizados para personalizar la apariencia de estos números de página.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Después de insertar estos campos XE, el campo ÍNDICE mostrará "Primera entrada, en las páginas 2, 3 y 4".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
