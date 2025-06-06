---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words para .NET
description: Descubra si la propiedad IsLinkToContent de DocumentProperty se conecta al contenido. Optimice su flujo de trabajo con soluciones de gestión documental integradas.
type: docs
weight: 10
url: /es/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Muestra si esta propiedad está vinculada al contenido o no.

```csharp
public bool IsLinkToContent { get; }
```

## Ejemplos

Muestra cómo vincular una propiedad de documento personalizada a un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

Vincular una nueva propiedad personalizada a un marcador. El valor de esta propiedad
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
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
