---
title: DocumentProperty.LinkSource
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentProperty propiedad. Obtiene el origen de una propiedad de documento personalizado vinculado.
type: docs
weight: 20
url: /es/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Obtiene el origen de una propiedad de documento personalizado vinculado.

```csharp
public string LinkSource { get; }
```

### Ejemplos

Muestra cómo vincular una propiedad de documento personalizada a un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Vincular una nueva propiedad personalizada a un marcador. El valor de esta propiedad
// será el contenido del marcador al que hace referencia en el miembro "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Ver también

* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../documentproperty/)
* asamblea [Aspose.Words](../../../)


