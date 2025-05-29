---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font Bidi, controle las características del texto de derecha a izquierda para mejorar la legibilidad y la experiencia del usuario en sus diseños web.
type: docs
weight: 30
url: /es/net/aspose.words/font/bidi/
---
## Font.Bidi property

Especifica si el contenido de esta ejecución tendrá características de derecha a izquierda.

```csharp
public bool Bidi { get; set; }
```

## Observaciones

Esta propiedad, cuando está activada, no se utilizará con texto con una fuerte inclinación de izquierda a derecha. Cualquier comportamiento bajo esta condición no se especifica. Esta propiedad, cuando está desactivada, no se utilizará con texto con una fuerte inclinación de derecha a izquierda. Cualquier comportamiento bajo esta condición no se especifica.

Al mostrar el contenido de esta ejecución, todos los caracteres se considerarán caracteres de script complejos para fines de formatting . Esto significa que[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) y se utilizará un nombre de fuente correspondiente al renderizar esta ejecución.

Además, cuando se muestra el contenido de esta ejecución, esta propiedad actúa como una anulación de derecha a izquierda para los caracteres que se clasifican como "tipos débiles" y "tipos neutrales".

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
