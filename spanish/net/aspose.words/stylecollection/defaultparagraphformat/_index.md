---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words para .NET
description: StyleCollection DefaultParagraphFormat propiedad. Obtiene el formato de párrafo predeterminado del documento en C#.
type: docs
weight: 30
url: /es/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Obtiene el formato de párrafo predeterminado del documento.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Observaciones

Tenga en cuenta que los valores predeterminados para todo el documento se introdujeron en Microsoft Word 2007 y son totalmente compatibles con los formatos OOXML (Docx) únicamente. Los formatos de documentos anteriores no admiten el formato de párrafo predeterminado del documento.

## Ejemplos

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

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
