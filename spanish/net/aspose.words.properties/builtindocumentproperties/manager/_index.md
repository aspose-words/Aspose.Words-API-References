---
title: BuiltInDocumentProperties.Manager
linktitle: Manager
articleTitle: Manager
second_title: Aspose.Words para .NET
description: Gestione fácilmente BuiltInDocumentProperties con nuestra herramienta intuitiva. Obtenga o configure propiedades fácilmente para optimizar su gestión de documentos.
type: docs
weight: 210
url: /es/net/aspose.words.properties/builtindocumentproperties/manager/
---
## BuiltInDocumentProperties.Manager property

Obtiene o establece la propiedad del administrador.

```csharp
public string Manager { get; set; }
```

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
