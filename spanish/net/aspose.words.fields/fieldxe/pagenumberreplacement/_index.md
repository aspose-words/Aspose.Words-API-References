---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldXE PageNumberReplacement para personalizar fácilmente el texto del número de página para mejorar el formato del documento y la legibilidad.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Obtiene o establece el texto utilizado en lugar de un número de página.

```csharp
public string PageNumberReplacement { get; set; }
```

## Ejemplos

Muestra cómo definir referencias cruzadas en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

//Podemos configurar un campo XE para que su entrada INDEX muestre una cadena en lugar de un número de página.
// Primero, para las entradas que sustituyen un número de página con una cadena,
// especifica un separador personalizado entre el valor de la propiedad Texto del campo XE y la cadena.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Inserta un campo XE, que crea una entrada INDEX normal que muestra el número de página de este campo,
// y no invoca el valor CrossReferenceSeparator.
//La entrada para este campo XE mostrará "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Inserte otro campo XE en la página 3 y establezca un valor para la propiedad PageNumberReplacement.
// Este valor se mostrará en lugar del número de la página en la que se encuentra este campo.
// y el valor CrossReferenceSeparator del campo INDEX aparecerá delante de él.
//La entrada para este campo XE mostrará "Plátano, ver: Fruta tropical".
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

* class [FieldXE](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
