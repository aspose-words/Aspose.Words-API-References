---
title: Font.LocaleIdBi
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece el identificador local idioma de los caracteres formateados de derecha a izquierda.
type: docs
weight: 210
url: /es/net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

Obtiene o establece el identificador local (idioma) de los caracteres formateados de derecha a izquierda.

```csharp
public int LocaleIdBi { get; set; }
```

### Observaciones

Para obtener la lista de identificadores locales, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

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


