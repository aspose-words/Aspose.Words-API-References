---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words para .NET
description: Descubra la propiedad DefaultFont de StyleCollection para un formato de texto uniforme. Mejore sus documentos con un estilo uniforme y profesional.
type: docs
weight: 20
url: /es/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Obtiene el formato de texto predeterminado del documento.

```csharp
public Font DefaultFont { get; }
```

## Observaciones

Tenga en cuenta que los valores predeterminados para todo el documento se introdujeron en Microsoft Word 2007 y son totalmente compatibles con los formatos OOXML (Docx) solamente. Los formatos de documentos anteriores tienen soporte limitado para esta función y solo se pueden almacenar nombres de fuentes.

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

* class [Font](../../font/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
