---
title: CustomDocumentProperties.Add
second_title: Referencia de API de Aspose.Words para .NET
description: CustomDocumentProperties método. Crea una nueva propiedad de documento personalizada delString tipo de datos.
type: docs
weight: 10
url: /es/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(string, string) {#add_4}

Crea una nueva propiedad de documento personalizada delString tipo de datos.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| value | String | El valor de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado.

### Ejemplos

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime todas las propiedades personalizadas del documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Costumbre".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../customdocumentproperties/)
* asamblea [Aspose.Words](../../../)

---

## Add(string, int) {#add_2}

Crea una nueva propiedad de documento personalizada delNumber tipo de datos.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| value | Int32 | El valor de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado.

### Ejemplos

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime todas las propiedades personalizadas del documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Costumbre".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../customdocumentproperties/)
* asamblea [Aspose.Words](../../../)

---

## Add(string, DateTime) {#add_3}

Crea una nueva propiedad de documento personalizada delDateTime tipo de datos.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| value | DateTime | El valor de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado.

### Ejemplos

Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y hora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime todas las propiedades personalizadas del documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Costumbre".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../customdocumentproperties/)
* asamblea [Aspose.Words](../../../)

---

## Add(string, bool) {#add}

Crea una nueva propiedad de documento personalizada delBoolean tipo de datos.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| value | Boolean | El valor de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado.

### Ejemplos

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime todas las propiedades personalizadas del documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Costumbre".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../customdocumentproperties/)
* asamblea [Aspose.Words](../../../)

---

## Add(string, double) {#add_1}

Crea una nueva propiedad de documento personalizada delDouble tipo de datos.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad. |
| value | Double | El valor de la propiedad. |

### Valor_devuelto

El objeto de propiedad recién creado.

### Ejemplos

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime todas las propiedades personalizadas del documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Costumbre".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../customdocumentproperties/)
* asamblea [Aspose.Words](../../../)


