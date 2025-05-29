---
title: FieldIndex.Heading
linktitle: Heading
articleTitle: Heading
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldIndex Heading para personalizar los encabezados de entrada por letra, mejorando la organización y la experiencia del usuario en su aplicación.
type: docs
weight: 70
url: /es/net/aspose.words.fields/fieldindex/heading/
---
## FieldIndex.Heading property

Obtiene o establece un encabezado que aparece al comienzo de cada conjunto de entradas para cualquier letra determinada.

```csharp
public string Heading { get; set; }
```

## Ejemplos

Muestra cómo rellenar un campo ÍNDICE con entradas utilizando campos XE y también modificar su apariencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
//el campo ÍNDICE los agrupará en una entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Establecer el valor de esta propiedad en "A" agrupará todas las entradas por su primera letra,
// y coloca esa letra en mayúscula encima de cada grupo.
index.Heading = "A";

// Establezca la tabla creada por el campo INDEX para que abarque 2 columnas.
index.NumberOfColumns = "2";

// Establezca cualquier entrada con letras iniciales fuera del rango de caracteres "ac" para que se omita.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Estos próximos dos campos XE aparecerán bajo el encabezado "A",
// con sus respectivos estilos de texto aplicados también a sus números de página.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Los siguientes dos campos XE estarán bajo un encabezado "B" y "C" en la tabla de contenido de los campos ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Los campos ÍNDICE ordenan todas las entradas alfabéticamente, por lo que esta entrada aparecerá debajo de "A" con las otras dos.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

//Esta entrada no aparecerá porque empieza con la letra "D",
// que está fuera del rango de caracteres "ac" que define la propiedad LetterRange del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
