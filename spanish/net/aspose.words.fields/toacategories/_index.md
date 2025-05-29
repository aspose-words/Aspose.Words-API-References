---
title: ToaCategories Class
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.ToaCategories para gestionar eficientemente las categorías de la tabla de autoridades en sus documentos. ¡Mejore la estructura de sus documentos!
type: docs
weight: 3190
url: /es/net/aspose.words.fields/toacategories/
---
## ToaCategories class

Representa una tabla de categorías de autoridades.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class ToaCategories
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ToaCategories](toacategories/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| static [DefaultCategories](../../aspose.words.fields/toacategories/defaultcategories/) { get; } | Obtiene la tabla predeterminada de categorías de autoridades. |
| [Item](../../aspose.words.fields/toacategories/item/) { get; set; } | Obtiene o establece el encabezado de categoría por número de categoría. |

## Ejemplos

Muestra cómo especificar un conjunto de categorías para los campos TOA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Los campos TOA pueden filtrar sus entradas por categorías definidas en esta colección.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

//Esta colección de categorías viene con valores predeterminados, que podemos sobrescribir con valores personalizados.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

//Siempre podemos acceder a los valores predeterminados a través de esta colección.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Insertar 2 campos TOA. Los campos TOA crean una entrada para cada campo TA en el documento.
// Utilice el interruptor "\c" para seleccionar el índice de una categoría de nuestra colección.
// Con este cambio, un campo TOA solo recogerá entradas de campos TA que
// También se incluye un modificador "\c" con un índice de categoría coincidente. Cada campo TOA también mostrará
// el nombre de la categoría a la que apunta su interruptor "\c".
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Insertar entradas TOA en 2 categorías. Nuestro primer campo TOA recibirá una entrada.
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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
