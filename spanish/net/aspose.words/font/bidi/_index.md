---
title: Font.Bidi
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Especifica si el contenido de esta ejecución tendrá características de derecha a izquierda.
type: docs
weight: 30
url: /es/net/aspose.words/font/bidi/
---
## Font.Bidi property

Especifica si el contenido de esta ejecución tendrá características de derecha a izquierda.

```csharp
public bool Bidi { get; set; }
```

### Observaciones

Esta propiedad, cuando está activada, no se debe utilizar con texto que se escribe fuertemente de izquierda a derecha. Cualquier comportamiento bajo esa condición no está especificado. Esta propiedad, cuando está desactivada, no se utilizará con texto fuerte de derecha a izquierda. Cualquier comportamiento bajo esa condición no está especificado.

Cuando se muestre el contenido de esta ejecución, todos los caracteres se tratarán como caracteres de secuencia de comandos complejos a efectos de formatear . Esto significa que[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) y se utilizará una fuente correspondiente name al renderizar esta ejecución.

Además, cuando se muestra el contenido de esta ejecución, esta propiedad actúa como una anulación de derecha a izquierda para los caracteres que se clasifican como "tipos débiles" y "tipos neutrales".

### Ejemplos

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda y de derecha a izquierda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definir un conjunto de configuraciones de fuente para texto de izquierda a derecha.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definir otro conjunto de configuraciones de fuente para texto de derecha a izquierda.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Podemos usar la bandera Bidi para indicar si el texto que estamos a punto de agregar
// con el generador de documentos es de derecha a izquierda. Cuando agregamos texto con este indicador establecido en verdadero,
// se formateará utilizando el conjunto de configuraciones de fuente de derecha a izquierda.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Establece la bandera en falso y luego agrega texto de izquierda a derecha.
// El creador de documentos los formateará utilizando el conjunto de configuraciones de fuente de izquierda a derecha.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


