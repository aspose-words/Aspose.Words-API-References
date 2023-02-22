---
title: Class FontSettings
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.FontSettings clase. Especifica la configuración de fuente para un documento.
type: docs
weight: 2790
url: /es/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Especifica la configuración de fuente para un documento.

```csharp
public class FontSettings
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FontSettings](fontsettings/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Configuración de fuente predeterminada estática. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Ajustes relacionados con el mecanismo de reserva de fuentes. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Ajustes relacionados con el mecanismo de sustitución de fuentes. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Obtiene una copia de la matriz que contiene la lista de fuentes donde Aspose.Words busca fuentes TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Restablece las fuentes de fuentes a los valores predeterminados del sistema. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(Stream) | Guarda la caché de búsqueda de fuentes en la secuencia. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(string, bool) | Establece la carpeta donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. Este es un acceso directo a[`SetFontsFolders`](./setfontsfolders/) para configurar solo un directorio de fuentes. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(string[], bool) | Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(FontSourceBase[]) | Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(FontSourceBase[], Stream) | Establece las fuentes en las que Aspose.Words busca las fuentes TrueType y, además, carga la caché de búsqueda de fuentes previamente guardada. |

### Observaciones

Aspose.Words usa la configuración de fuente para resolver las fuentes en el documento. Las fuentes se resuelven principalmente al crear el diseño del documento o al renderizar a formatos de página fijos. Pero al cargar algunos formatos, Aspose.Words también puede requerir resolver las fuentes. Por ejemplo, when cargar documentos HTML, Aspose.Words puede resolver las fuentes para realizar una reserva de fuentes. Por lo tanto, se recomienda que establezca la configuración de fuente en [`LoadOptions`](../../aspose.words.loading/loadoptions/) al cargar el documento. O al menos antes de crear el diseño o representar el documento en el formato de página fija.

De forma predeterminada, todos los documentos utilizan una sola instancia de configuración de fuente estática. Se puede acceder por [`DefaultInstance`](./defaultinstance/) propiedad.

Cambiar la configuración de la fuente es seguro en cualquier momento desde cualquier hilo. Pero se recomienda que no cambie la configuración de la fuente mientras procesa algunos documentos que utilizan esta configuración. Esto puede llevar al hecho de que la misma fuente se resuelva de manera diferente en diferentes partes del documento.

### Ejemplos

Muestra cómo agregar una fuente de fuente a nuestras fuentes de fuente existentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// A la fuente de fuente predeterminada le faltan dos de las fuentes que estamos usando en nuestro documento.
// Cuando guardemos este documento, Aspose.Words aplicará fuentes alternativas a todo el texto formateado con fuentes inaccesibles.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Cree una fuente de fuentes a partir de una carpeta que contenga fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Aplicar una nueva matriz de fuentes de fuentes que contenga las fuentes de fuentes originales, así como nuestras fuentes personalizadas.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifique que Aspose.Words tenga acceso a todas las fuentes requeridas antes de convertir el documento en PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Muestra cómo configurar un directorio fuente de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de fuentes no contienen la fuente que hemos usado para el texto en este documento.
// Si usamos esta configuración de fuente mientras renderizamos este documento,
// Aspose.Words aplicará una fuente alternativa al texto que tenga una fuente que Aspose.Words no pueda localizar.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// A las fuentes de fuentes predeterminadas les faltan las dos fuentes que estamos usando en este documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Use el método "SetFontsFolder" para establecer un directorio que actuará como una nueva fuente de fuente.
// Pase "falso" como argumento "recursivo" para incluir fuentes de todos los archivos de fuentes que están en el directorio
// que estamos pasando en el primer argumento, pero sin incluir ninguna fuente en ninguna de las subcarpetas de ese directorio.
// Pasar "verdadero" como argumento "recursivo" para incluir todos los archivos de fuentes en el directorio que estamos pasando
// en el primer argumento, así como todas las fuentes en sus subdirectorios.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// La fuente "Amethysta" está en una subcarpeta del directorio de fuentes.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Muestra cómo establecer varios directorios de fuentes de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de fuentes no contienen la fuente que hemos usado para el texto en este documento.
// Si usamos esta configuración de fuente mientras renderizamos este documento,
// Aspose.Words aplicará una fuente alternativa al texto que tenga una fuente que Aspose.Words no pueda localizar.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// A las fuentes de fuentes predeterminadas les faltan las dos fuentes que estamos usando en este documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Use el método "SetFontsFolders" para crear una fuente de fuente de cada directorio de fuentes que pasemos como primer argumento.
// Pase "falso" como argumento "recursivo" para incluir fuentes de todos los archivos de fuentes que están en los directorios
// que estamos pasando en el primer argumento, pero sin incluir ninguna fuente de ninguna de las subcarpetas de los directorios.
// Pasar "verdadero" como argumento "recursivo" para incluir todos los archivos de fuentes en los directorios que estamos pasando
// en el primer argumento, así como todas las fuentes en sus subdirectorios.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// La carpeta "Junction" en sí no contiene archivos de fuentes, pero tiene subcarpetas que sí.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


