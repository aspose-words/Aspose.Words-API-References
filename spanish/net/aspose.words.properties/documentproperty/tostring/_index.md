---
title: DocumentProperty.ToString
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentProperty método. Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual.
type: docs
weight: 110
url: /es/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual.

```csharp
public override string ToString()
```

### Observaciones

Convierte una propiedad booleana en "Y" o "N". Convierte una propiedad de fecha en una cadena de fecha corta. Para todos los demás tipos, convierte una propiedad usando Object.ToString().

### Ejemplos

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

Muestra cómo trabajar con propiedades de documentos personalizados.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Cada documento contiene una colección de propiedades personalizadas que, al igual que las propiedades integradas, son pares clave-valor.
 // El documento tiene una lista fija de propiedades integradas. El usuario crea todas las propiedades personalizadas.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Ver también

* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../documentproperty/)
* asamblea [Aspose.Words](../../../)


