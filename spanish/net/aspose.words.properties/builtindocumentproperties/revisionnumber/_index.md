---
title: BuiltInDocumentProperties.RevisionNumber
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Obtiene o establece el número de revisión del documento.
type: docs
weight: 240
url: /es/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Obtiene o establece el número de revisión del documento.

```csharp
public int RevisionNumber { get; set; }
```

### Observaciones

Aspose.Words no actualiza esta propiedad.

### Ejemplos

Muestra cómo trabajar con campos REVNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Inserte un campo REVNUM, que muestra la propiedad del número de revisión actual del documento.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Esta propiedad cuenta cuantas veces se ha guardado un documento en Microsoft Word,
// y no está relacionado con las revisiones registradas. Podemos encontrarlo haciendo clic derecho en el documento en el Explorador de Windows
// vía Propiedades -> Detalles. Podemos actualizar esta propiedad manualmente.
doc.BuiltInDocumentProperties.RevisionNumber++;

Assert.AreEqual("2", field.Result);
```

Muestra cómo trabajar con propiedades de documentos en la categoría "Origen".

```csharp
// Abrir un documento que hayamos creado y editado con Microsoft Word.
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


