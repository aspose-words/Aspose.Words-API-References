---
title: Font.ItalicBi
linktitle: ItalicBi
articleTitle: ItalicBi
second_title: Aspose.Words para .NET
description: Descubra la propiedad ItalicBi para fuentes, mejore el formato de texto de derecha a izquierda con estilos cursivos para una mejor legibilidad y un diseño atractivo.
type: docs
weight: 170
url: /es/net/aspose.words/font/italicbi/
---
## Font.ItalicBi property

Verdadero si el texto de derecha a izquierda está formateado en cursiva.

```csharp
public bool ItalicBi { get; set; }
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
