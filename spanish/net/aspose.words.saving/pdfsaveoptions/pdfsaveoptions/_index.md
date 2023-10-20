---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words para .NET
description: PdfSaveOptions constructor. Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en Pdf formato en C#.
type: docs
weight: 10
url: /es/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en Pdf formato.

```csharp
public PdfSaveOptions()
```

## Ejemplos

Muestra cómo habilitar o deshabilitar el subconjunto al incrustar fuentes mientras se procesa un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configure nuestras fuentes de fuentes para asegurarnos de que tengamos acceso a ambas fuentes en este documento.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Dado que nuestro documento contiene una fuente personalizada, puede ser conveniente incrustarla en el documento de salida.
// Establece la propiedad "EmbedFullFonts" en "true" para incrustar cada glifo de cada fuente incrustada en el PDF de salida.
// El tamaño del documento puede llegar a ser muy grande, pero podremos utilizar todas las fuentes al máximo si editamos el PDF.
// Establece la propiedad "EmbedFullFonts" en "false" para aplicar subconjuntos a las fuentes, guardando solo los glifos
// que el documento está utilizando. El archivo será considerablemente más pequeño,
// pero es posible que necesitemos acceso a fuentes personalizadas si editamos el documento.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
