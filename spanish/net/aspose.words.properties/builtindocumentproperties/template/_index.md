---
title: BuiltInDocumentProperties.Template
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Obtiene o establece el nombre informativo de la plantilla del documento.
type: docs
weight: 270
url: /es/net/aspose.words.properties/builtindocumentproperties/template/
---
## BuiltInDocumentProperties.Template property

Obtiene o establece el nombre informativo de la plantilla del documento.

```csharp
public string Template { get; set; }
```

### Observaciones

En Microsoft Word, esta propiedad tiene solo fines informativos y generalmente contiene solo el nombre del archivo de la plantilla sin la ruta.

Cadena vacía significa que el documento está adjunto a la plantilla Normal.

Para obtener o establecer el nombre real de la plantilla adjunta, utilice the [`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) propiedad.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Properties](../../builtindocumentproperties/)
* asamblea [Aspose.Words](../../../)


