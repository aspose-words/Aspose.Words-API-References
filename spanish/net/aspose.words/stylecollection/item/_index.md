---
title: StyleCollection.Item
second_title: Referencia de API de Aspose.Words para .NET
description: StyleCollection propiedad. Obtiene un estilo por nombre o alias.
type: docs
weight: 50
url: /es/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Obtiene un estilo por nombre o alias.

```csharp
public Style this[string name] { get; }
```

### Observaciones

Distingue entre mayúsculas y minúsculas, devuelve`nulo` si no se encuentra el estilo con el nombre de pila.

Si se trata de un nombre en inglés de un estilo integrado que aún no existe, lo crea automáticamente.

### Ejemplos

Muestra cuándo volver a calcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez se realizará automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // En la versión actual de Aspose.Words, la modificación del documento no se reconstruye automáticamente
// el diseño de la página en caché. Si deseamos el diseño en caché
// para mantenernos actualizados, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ver también

* class [Style](../../style/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Obtiene un estilo integrado por su identificador independiente de configuración regional.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/) valor que especifica el estilo integrado que se recuperará. |

### Observaciones

Al acceder a un estilo que aún no existe, lo crea automáticamente.

### Ejemplos

Muestra cómo agregar un estilo a la colección de estilos de un documento.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Establece parámetros predeterminados para nuevos estilos que luego podremos agregar a esta colección.
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
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Obtiene un estilo por index.

```csharp
public Style this[int index] { get; }
```

### Ejemplos

Muestra cómo agregar un estilo a la colección de estilos de un documento.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Establece parámetros predeterminados para nuevos estilos que luego podremos agregar a esta colección.
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
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)


