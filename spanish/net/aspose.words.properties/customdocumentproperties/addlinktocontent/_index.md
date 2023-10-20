---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words para .NET
description: CustomDocumentProperties AddLinkToContent método. Crea una nueva propiedad de documento personalizada vinculada al contenido en C#.
type: docs
weight: 20
url: /es/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Crea una nueva propiedad de documento personalizada vinculada al contenido.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| linkSource | String | La fuente de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado o`nulo` cuando el*linkSource* es inválido.

## Ejemplos

Muestra cómo vincular una propiedad de documento personalizada a un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Vincular una nueva propiedad personalizada a un marcador. El valor de esta propiedad.
// será el contenido del marcador al que hace referencia en el miembro "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
