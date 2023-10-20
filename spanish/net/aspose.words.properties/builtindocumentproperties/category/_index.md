---
title: BuiltInDocumentProperties.Category
linktitle: Category
articleTitle: Category
second_title: Aspose.Words para .NET
description: BuiltInDocumentProperties Category propiedad. Obtiene o establece la categoría del documento en C#.
type: docs
weight: 30
url: /es/net/aspose.words.properties/builtindocumentproperties/category/
---
## BuiltInDocumentProperties.Category property

Obtiene o establece la categoría del documento.

```csharp
public string Category { get; set; }
```

## Ejemplos

Muestra cómo trabajar con propiedades de documentos integradas en la categoría "Descripción".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// A continuación se muestran cuatro propiedades de documento integradas que tienen campos que pueden mostrar sus valores en el cuerpo del documento.
// 1 - Propiedad "Autor", que podemos mostrar usando un campo AUTOR:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Propiedad "Título", que podemos mostrar usando un campo TÍTULO:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Propiedad "Asunto", que podemos mostrar usando un campo ASUNTO:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Propiedad "Comentarios", que podemos mostrar usando un campo COMENTARIOS:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// La propiedad incorporada "Categoría" no tiene un campo que pueda mostrar su valor.
properties.Category = "My category";

// Podemos establecer varias palabras clave para un documento separando el valor de cadena de la propiedad "Palabras clave" con punto y coma.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Podemos hacer clic derecho en este documento en el Explorador de Windows y encontrar estas propiedades en "Propiedades" -> "Detalles".
// La propiedad integrada "Autor" está en el grupo "Origen" y las demás están en el grupo "Descripción".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
