---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words para .NET
description: Descubre la función BuiltInDocumentProperties LastPrinted para rastrear fácilmente la última fecha de impresión de tu documento en UTC. ¡Mejora tu flujo de trabajo hoy mismo!
type: docs
weight: 160
url: /es/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Obtiene o establece la fecha en la que se imprimió el documento por última vez en UTC.

```csharp
public DateTime LastPrinted { get; set; }
```

## Observaciones

Para los documentos originados en formato RTF, esta propiedad devuelve la hora local de la última operación de impresión.

Si el documento nunca se imprimió, esta propiedad devolverá DateTime.MinValue.

Aspose.Words no actualiza esta propiedad.

## Ejemplos

Muestra cómo trabajar con las propiedades del documento en la categoría "Origen".

```csharp
//Abrimos un documento que hemos creado y editado usando Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

//Las siguientes propiedades integradas contienen información sobre la creación y edición de este documento.
//Podemos hacer clic derecho en este documento en el Explorador de Windows y buscar
// estas propiedades a través de la categoría "Propiedades" -> "Detalles" -> "Origen".
// Los campos como PRINTDATE y EDITTIME pueden mostrar estos valores en el cuerpo del documento.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// También podemos cambiar los valores de las propiedades incorporadas.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

//Microsoft Word actualiza las siguientes propiedades automáticamente cuando guardamos el documento.
// Para utilizar estas propiedades con Aspose.Words, necesitaremos establecer valores para ellas manualmente.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

//Podemos hacer clic derecho en este documento en el Explorador de Windows y buscar these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
