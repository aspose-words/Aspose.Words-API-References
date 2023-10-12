---
title: CleanupOptions.DuplicateStyle
second_title: Referencia de API de Aspose.Words para .NET
description: CleanupOptions propiedad. Obtiene/establece un indicador que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado esFALSO .
type: docs
weight: 20
url: /es/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Obtiene/establece un indicador que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado es`FALSO` .

```csharp
public bool DuplicateStyle { get; set; }
```

### Ejemplos

Muestra cómo eliminar estilos duplicados del documento.

```csharp
Document doc = new Document();

// Agrega dos estilos al documento con propiedades idénticas,
// pero nombres diferentes. El segundo estilo se considera un duplicado del primero.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Aplicar ambos estilos a diferentes párrafos dentro del documento.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Configura un objeto CleanOptions, luego llama al método Cleanup para sustituir todos los estilos duplicados
// con el original y eliminar los duplicados del documento.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Ver también

* class [CleanupOptions](../)
* espacio de nombres [Aspose.Words](../../cleanupoptions/)
* asamblea [Aspose.Words](../../../)


