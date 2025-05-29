---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: ¡Descubra la poderosa propiedad Item de StyleCollection para recuperar estilos sin esfuerzo por nombre o alias, mejorando su experiencia de diseño con facilidad!
type: docs
weight: 50
url: /es/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Obtiene un estilo por nombre o alias.

```csharp
public Style this[string name] { get; }
```

## Observaciones

Sensible a mayúsculas y minúsculas, devuelve`nulo` Si no se encuentra el estilo con el nombre dado.

Si se trata de un nombre en inglés de un estilo incorporado que aún no existe, lo crea automáticamente.

## Ejemplos

Muestra cuándo recalcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento como PDF, como imagen o imprimirlo por primera vez se realizará automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// En la versión actual de Aspose.Words, modificar el documento no lo reconstruye automáticamente
// El diseño de la página en caché. Si deseamos el diseño en caché
// Para mantenernos actualizados, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ver también

* class [Style](../../style/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Obtiene un estilo incorporado por su identificador independiente de la configuración regional.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) valor que especifica el estilo integrado a recuperar. |

## Observaciones

Al acceder a un estilo que aún no existe, lo crea automáticamente.

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

### Ver también

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Obtiene un estilo por índice.

```csharp
public Style this[int index] { get; }
```

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

### Ver también

* class [Style](../../style/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
