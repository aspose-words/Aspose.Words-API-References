---
title: FieldOptions.ToaCategories
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words para .NET
description: FieldOptions ToaCategories propiedad. Obtiene o establece la tabla de categorías de autoridades en C#.
type: docs
weight: 200
url: /es/net/aspose.words.fields/fieldoptions/toacategories/
---
## FieldOptions.ToaCategories property

Obtiene o establece la tabla de categorías de autoridades.

```csharp
public ToaCategories ToaCategories { get; set; }
```

## Ejemplos

Muestra cómo especificar un conjunto de categorías para campos TOA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos TOA pueden filtrar sus entradas por categorías definidas en esta colección.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Esta colección de categorías viene con valores predeterminados, que podemos sobrescribir con valores personalizados.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Siempre podemos acceder a los valores predeterminados a través de esta colección.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Inserta 2 campos TOA. Los campos TOA crean una entrada para cada campo TA en el documento.
// Utilice el interruptor "\c" para seleccionar el índice de una categoría de nuestra colección.
// Con este cambio, un campo TOA solo recogerá entradas de campos TA que
// también tenemos un modificador "\c" con un índice de categoría coincidente. Cada campo TOA también mostrará
// el nombre de la categoría a la que apunta su modificador "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Inserta entradas TOA en 2 categorías. Nuestro primer campo TOA recibirá una entrada,
// del segundo campo TA cuyo modificador "\c" también apunta a la primera categoría.
// El segundo campo TOA tendrá dos entradas de los otros dos campos TA.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Ver también

* class [ToaCategories](../../toacategories/)
* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
