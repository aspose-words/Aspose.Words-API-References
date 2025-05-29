---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Descubra el método StyleCollection Add para crear y agregar sin esfuerzo estilos personalizados definidos por el usuario a su colección, mejorando su flexibilidad de diseño.
type: docs
weight: 60
url: /es/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Crea un nuevo estilo definido por el usuario y lo agrega a la colección.

```csharp
public Style Add(StyleType type, string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| type | StyleType | A[`StyleType`](../../styletype/) valor que especifica el tipo de estilo a crear. |
| name | String | Nombre del estilo que se va a crear que distingue entre mayúsculas y minúsculas. |

## Observaciones

Puedes crear un estilo de carácter, de párrafo o de lista.

Al crear un estilo de lista, el estilo se crea con el formato de lista numerada predeterminado (1 \ a \ i).

Lanza una excepción si ya existe un estilo con este nombre.

## Ejemplos

Muestra cómo agregar un estilo a la colección de estilos de un documento.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Establezca parámetros predeterminados para nuevos estilos que podamos agregar más adelante a esta colección.
styles.DefaultFont.Name = "Courier New";
// Si agregamos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
// su propiedad "DefaultParagraphFormat" a la propiedad "ParagraphFormat" del estilo.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Agregue un estilo y luego verifique que tenga la configuración predeterminada.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

Muestra cómo crear un estilo de lista y usarlo en un documento.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
//Podemos contener un objeto Lista completo dentro de un estilo.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Cambiar la apariencia de todos los niveles de lista en nuestra lista.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Crea otra lista a partir de una lista dentro de un estilo.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Agregue algunos elementos de lista que nuestra lista formateará.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crea y aplica otra lista basada en el estilo de lista.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Ver también

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
