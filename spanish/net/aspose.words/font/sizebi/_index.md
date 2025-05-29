---
title: Font.SizeBi
linktitle: SizeBi
articleTitle: SizeBi
second_title: Aspose.Words para .NET
description: Ajuste fácilmente el tamaño de fuente en puntos para documentos de derecha a izquierda. Mejore la legibilidad y el diseño con nuestra sencilla función Font SizeBi.
type: docs
weight: 360
url: /es/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Obtiene o establece el tamaño de fuente en puntos utilizado en un documento de derecha a izquierda.

```csharp
public double SizeBi { get; set; }
```

## Ejemplos

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda y de derecha a izquierda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Define un conjunto de configuraciones de fuente para texto de izquierda a derecha.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Define otro conjunto de configuraciones de fuente para texto de derecha a izquierda.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

//Podemos usar la bandera Bidi para indicar si el texto que estamos a punto de agregar
// con el generador de documentos es de derecha a izquierda. Cuando agregamos texto con este indicador establecido en verdadero,
//Se formateará utilizando el conjunto de configuraciones de fuente de derecha a izquierda.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Establezca la bandera en falso y luego agregue texto de izquierda a derecha.
// El generador de documentos les dará formato utilizando el conjunto de configuraciones de fuente de izquierda a derecha.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
