---
title: Font.ItalicBi
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si el texto de derecha a izquierda tiene formato de cursiva.
type: docs
weight: 170
url: /es/net/aspose.words/font/italicbi/
---
## Font.ItalicBi property

Verdadero si el texto de derecha a izquierda tiene formato de cursiva.

```csharp
public bool ItalicBi { get; set; }
```

### Ejemplos

Muestra cómo definir conjuntos separados de configuración de fuente para texto de derecha a izquierda y de derecha a izquierda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definir un conjunto de configuraciones de fuente para el texto de izquierda a derecha.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definir otro conjunto de configuraciones de fuente para el texto de derecha a izquierda.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Podemos usar la bandera Bidi para indicar si el texto que vamos a agregar
// con el generador de documentos es de derecha a izquierda. Cuando agregamos texto con esta bandera establecida en verdadero,
// se formateará usando el conjunto de configuraciones de fuente de derecha a izquierda.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Establezca el indicador en falso y luego agregue texto de izquierda a derecha.
// El generador de documentos los formateará utilizando el conjunto de configuraciones de fuente de izquierda a derecha.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


