---
title: DocumentBuilder.InsertStyleSeparator
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta un separador de estilo en el documento.
type: docs
weight: 460
url: /es/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Inserta un separador de estilo en el documento.

```csharp
public void InsertStyleSeparator()
```

### Observaciones

Este método permite aplicar diferentes estilos de párrafo a dos partes diferentes de una línea de texto.

### Ejemplos

Muestra cómo trabajar con separadores de estilos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo sólo puede tener un estilo.
// El método InsertStyleSeparator nos permite solucionar esta limitación.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Llamar al método InsertStyleSeparator crea otro párrafo,
// que puede tener un estilo diferente al anterior. No habrá pausa entre párrafos.
// El texto del documento de salida se verá como un párrafo con dos estilos.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


