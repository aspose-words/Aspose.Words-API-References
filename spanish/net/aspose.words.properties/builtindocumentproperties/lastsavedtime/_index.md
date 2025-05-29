---
title: BuiltInDocumentProperties.LastSavedTime
linktitle: LastSavedTime
articleTitle: LastSavedTime
second_title: Aspose.Words para .NET
description: Descubra la propiedad BuiltInDocumentProperties LastSavedTime para rastrear fácilmente la última hora de guardado de su documento en UTC. ¡Mejore su gestión documental hoy mismo!
type: docs
weight: 180
url: /es/net/aspose.words.properties/builtindocumentproperties/lastsavedtime/
---
## BuiltInDocumentProperties.LastSavedTime property

Obtiene o establece la hora del último guardado en UTC.

```csharp
public DateTime LastSavedTime { get; set; }
```

## Observaciones

Para los documentos originados en formato RTF, esta propiedad devuelve la hora local de la última operación de guardado.

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

Muestra cómo utilizar el campo SAVEDATE para mostrar la fecha y hora de la operación de guardado más reciente del documento realizada con Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

//Podemos utilizar el campo SAVEDATE para mostrar la fecha y hora de la última operación de guardado en el documento.
// La operación de guardado a la que se refieren estos campos es el guardado manual en una aplicación como Microsoft Word,
// no es el método Guardar del documento.
// A continuación se muestran tres tipos de calendario diferentes según los cuales el campo SAVEDATE puede mostrar la fecha/hora.
// 1 - Calendario lunar islámico:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Calendario de Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Calendario nacional indio:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Los campos SAVEDATE obtienen sus valores de fecha y hora de la propiedad incorporada LastSavedTime.
// El método Guardar del documento no actualizará este valor, pero aún podemos actualizarlo manualmente.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
