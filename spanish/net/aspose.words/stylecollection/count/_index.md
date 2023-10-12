---
title: StyleCollection.Count
second_title: Referencia de API de Aspose.Words para .NET
description: StyleCollection propiedad. Obtiene el número de estilos de la colección.
type: docs
weight: 10
url: /es/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Obtiene el número de estilos de la colección.

```csharp
public int Count { get; }
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

* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)


