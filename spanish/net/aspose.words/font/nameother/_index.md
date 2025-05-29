---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words para .NET
description: Descubre Font NameOther. Personaliza fácilmente las fuentes para los códigos de caracteres 128-255, mejorando el estilo y la legibilidad de tu texto. ¡Mejora tu diseño hoy mismo!
type: docs
weight: 270
url: /es/net/aspose.words/font/nameother/
---
## Font.NameOther property

Devuelve o establece la fuente utilizada para caracteres con códigos de caracteres del 128 al 255.

```csharp
public string NameOther { get; set; }
```

## Ejemplos

Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en una sola ejecución.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supongamos una ejecución en la que usamos el constructor para insertar mientras usamos esta configuración de fuente
// contiene caracteres dentro del rango de caracteres ASCII. En ese caso,
//Mostrará aquellos caracteres que usen esta fuente.
builder.Font.NameAscii = "Calibri";

// Si no se especifica ninguna otra fuente, el generador también aplicará esta fuente a todos los caracteres que inserte.
Assert.AreEqual("Calibri", builder.Font.Name);

// Especifique una fuente para usar para todos los caracteres fuera del rango ASCII.
// Idealmente, esta fuente debería tener un glifo para cada código de carácter no ASCII requerido.
builder.Font.NameOther = "Courier New";

// Inserte una ejecución con una palabra que consta de caracteres ASCII y una palabra con todos los caracteres fuera de ese rango.
// Cada carácter se mostrará utilizando una de las fuentes, según corresponda.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Ver también

* property [Name](../name/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
