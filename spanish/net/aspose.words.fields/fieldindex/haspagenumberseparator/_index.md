---
title: FieldIndex.HasPageNumberSeparator
linktitle: HasPageNumberSeparator
articleTitle: HasPageNumberSeparator
second_title: Aspose.Words para .NET
description: FieldIndex HasPageNumberSeparator propiedad. Obtiene un valor que indica si un separador de número de página se anula mediante el código del campo en C#.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

Obtiene un valor que indica si un separador de número de página se anula mediante el código del campo.

```csharp
public bool HasPageNumberSeparator { get; }
```

## Ejemplos

Muestra cómo editar el separador de número de página en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE que se encuentra en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada ÍNDICE agrupará los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Si nuestro campo ÍNDICE tiene una entrada para un grupo de campos XE,
// esta entrada mostrará el número de cada página que contiene un campo XE que pertenece a este grupo.
// Podemos establecer separadores personalizados para personalizar la apariencia de estos números de página.
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
