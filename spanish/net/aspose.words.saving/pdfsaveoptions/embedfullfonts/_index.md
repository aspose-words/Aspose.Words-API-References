---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words para .NET
description: Descubra cómo la función PdfSaveOptions EmbedFullFonts mejora sus documentos PDF al garantizar la incrustación completa de fuentes para un formato perfecto.
type: docs
weight: 120
url: /es/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Controla cómo se incrustan las fuentes en los documentos PDF resultantes.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`, lo que significa que las fuentes se subdividen antes de incrustarlas. La subdivisión es útil si desea reducir el tamaño del archivo de salida. La subdivisión elimina todos los glifos no utilizados de una fuente.

Cuando este valor se establece en`verdadero`Se incrusta un archivo de fuente completo en el PDF sin subconjuntos. Esto genera archivos de salida más grandes, pero puede ser una opción útil si desea editar el PDF resultante posteriormente (por ejemplo, añadir más texto).

Algunas fuentes son grandes (varios megabytes) e incrustarlas sin subsetting dará como resultado documentos de salida grandes.

## Ejemplos

Muestra cómo habilitar o deshabilitar la creación de subconjuntos al incrustar fuentes al renderizar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configure nuestras fuentes para garantizar que tengamos acceso a ambas fuentes en este documento.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Dado que nuestro documento contiene una fuente personalizada, puede ser conveniente incrustarla en el documento de salida.
// Establezca la propiedad "EmbedFullFonts" en "true" para incrustar cada glifo de cada fuente incrustada en el PDF de salida.
//El tamaño del documento puede llegar a ser muy grande, pero tendremos uso completo de todas las fuentes si editamos el PDF.
// Establezca la propiedad "EmbedFullFonts" en "falso" para aplicar subconjuntos a las fuentes, guardando solo los glifos
// que utiliza el documento. El archivo será considerablemente más pequeño.
// pero es posible que necesitemos acceso a cualquier fuente personalizada si editamos el documento.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Restaurar las fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
