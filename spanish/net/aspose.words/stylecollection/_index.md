---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.StyleCollection, que incluye una amplia variedad de objetos de estilo integrados y personalizados para mejorar el formato y el diseño de su documento.
type: docs
weight: 6990
url: /es/net/aspose.words/stylecollection/
---
## StyleCollection class

Una colección de[`Style`](../style/)objetos que representan tanto los estilos integrados como los definidos por el usuario en un documento.

Para obtener más información, visite el[Trabajar con estilos y temas](https://docs.aspose.com/words/net/working-with-styles-and-themes/) Artículo de documentación.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Obtiene el número de estilos en la colección. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Obtiene el formato de texto predeterminado del documento. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Obtiene el formato de párrafo predeterminado del documento. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Obtiene el documento del propietario. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Obtiene un estilo por nombre o alias. (3 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Crea un nuevo estilo definido por el usuario y lo agrega a la colección. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Copia un estilo en esta colección. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Elimina todos los estilos del panel Galería de estilos rápidos. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Obtiene un objeto enumerador que enumerará los estilos en el orden alfabético de sus nombres. |

## Ejemplos

Muestra cómo crear y utilizar un estilo de párrafo con formato de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un estilo de párrafo personalizado.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Cree una lista y asegúrese de que los párrafos que usan este estilo usarán esta lista.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Aplique el estilo de párrafo al párrafo actual del generador de documentos y luego agregue algo de texto.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del generador de documentos a uno que no tenga formato de lista y escriba otro párrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ver también

* class [Style](../style/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
