---
title: ToDateTime
second_title: Referencia de API de Aspose.Words para .NET
description: Devuelve el valor de la propiedad como DateTime en UTC.
type: docs
weight: 80
url: /es/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Devuelve el valor de la propiedad como DateTime en UTC.

```csharp
public DateTime ToDateTime()
```

### Observaciones

Lanza una excepción si el tipo de propiedad no esDateTime.

Microsoft Word almacena solo la parte de la fecha (sin tiempo) para las propiedades de fecha personalizadas.

### Ejemplos

Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y una hora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Muestra varios métodos de conversión de tipos de propiedades de documentos personalizados.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### Ver también

* class [DocumentProperty](../../documentproperty)
* espacio de nombres [Aspose.Words.Properties](../../documentproperty)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->