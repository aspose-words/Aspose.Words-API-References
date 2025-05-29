---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad StyleCollection Count para recuperar fácilmente el número total de estilos en su colección para una mejor organización y administración.
type: docs
weight: 10
url: /es/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Obtiene el número de estilos en la colección.

```csharp
public int Count { get; }
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

* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
