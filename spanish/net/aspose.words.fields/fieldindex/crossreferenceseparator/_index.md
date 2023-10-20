---
title: FieldIndex.CrossReferenceSeparator
linktitle: CrossReferenceSeparator
articleTitle: CrossReferenceSeparator
second_title: Aspose.Words para .NET
description: FieldIndex CrossReferenceSeparator propiedad. Obtiene o establece la secuencia de caracteres que se utiliza para separar referencias cruzadas y otras entradas en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

Obtiene o establece la secuencia de caracteres que se utiliza para separar referencias cruzadas y otras entradas.

```csharp
public string CrossReferenceSeparator { get; set; }
```

## Ejemplos

Muestra cómo definir referencias cruzadas en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE que se encuentra en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada ÍNDICE recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Podemos configurar un campo XE para que su entrada ÍNDICE muestre una cadena en lugar de un número de página.
// Primero, para entradas que sustituyen un número de página por una cadena,
// especifica un separador personalizado entre el valor de la propiedad Texto del campo XE y la cadena.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Inserta un campo XE, que crea una entrada ÍNDICE normal que muestra el número de página de este campo,
// y no invoca el valor CrossReferenceSeparator.
// La entrada para este campo XE mostrará "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Inserte otro campo XE en la página 3 y establezca un valor para la propiedad PageNumberReplacement.
// Este valor aparecerá en lugar del número de la página en la que se encuentra este campo,
// y el valor CrossReferenceSeparator del campo ÍNDICE aparecerá delante de él.
// La entrada para este campo XE mostrará "Plátano, ver: Fruta tropical".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
