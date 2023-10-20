---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words para .NET
description: BuiltInDocumentProperties LastPrinted propiedad. Obtiene o establece la fecha en la que el documento se imprimió por última vez en UTC en C#.
type: docs
weight: 150
url: /es/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Obtiene o establece la fecha en la que el documento se imprimió por última vez en UTC.

```csharp
public DateTime LastPrinted { get; set; }
```

## Observaciones

Para documentos originados en formato RTF, esta propiedad devuelve la hora local de la última operación de impresión.

Si el documento nunca se imprimió, esta propiedad devolverá DateTime.MinValue.

Aspose.Words no actualiza esta propiedad.

## Ejemplos

Muestra cómo trabajar con propiedades de documentos en la categoría "Origen".

```csharp
//Abrir un documento que hemos creado y editado usando Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Las siguientes propiedades integradas contienen información sobre la creación y edición de este documento.
// Podemos hacer clic derecho en este documento en el Explorador de Windows y buscar
// estas propiedades a través de "Propiedades" -> "Detalles" -> Categoría "Origen".
// Campos como PRINTDATE y EDITTIME pueden mostrar estos valores en el cuerpo del documento.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// También podemos cambiar los valores de las propiedades integradas.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word actualiza las siguientes propiedades automáticamente cuando guardamos el documento.
// Para usar estas propiedades con Aspose.Words, necesitaremos establecer valores para ellas manualmente.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Podemos hacer clic derecho en este documento en el Explorador de Windows y buscar these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
