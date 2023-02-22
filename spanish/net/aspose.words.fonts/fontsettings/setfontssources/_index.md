---
title: FontSettings.SetFontsSources
second_title: Referencia de API de Aspose.Words para .NET
description: FontSettings método. Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes.
type: docs
weight: 100
url: /es/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

Establece las fuentes donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sources | FontSourceBase[] | Una matriz de fuentes que contienen fuentes TrueType. |

### Observaciones

De forma predeterminada, Aspose.Words busca las fuentes instaladas en el sistema.

Establecer esta propiedad restablece la memoria caché de todas las fuentes cargadas anteriormente.

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

### Ver también

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsettings/)
* asamblea [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

Establece las fuentes en las que Aspose.Words busca las fuentes TrueType y, además, carga la caché de búsqueda de fuentes previamente guardada.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| sources | FontSourceBase[] | Una matriz de fuentes que contienen fuentes TrueType. |
| cacheInputStream | Stream | Flujo de entrada con caché de búsqueda de fuente guardada. |

### Observaciones

Cargar la memoria caché de búsqueda de fuentes previamente guardada acelerará el proceso de inicialización de la memoria caché de fuentes. Es especialmente útil cuando el acceso a fuentes de fuentes es complicado (por ejemplo, cuando las fuentes se cargan a través de la red).

Al guardar y cargar la caché de búsqueda de fuentes, las fuentes en las fuentes proporcionadas se identifican a través de la clave de caché. Para las fuentes en el[`SystemFontSource`](../../systemfontsource/) y[`FolderFontSource`](../../folderfontsource/) la clave de caché es la ruta al archivo de fuente. Para[`MemoryFontSource`](../../memoryfontsource/) y[`StreamFontSource`](../../streamfontsource/) la clave de caché está definida en el[`CacheKey`](../../memoryfontsource/cachekey/) y[`CacheKey`](../../streamfontsource/cachekey/) propiedades respectivamente. Para el[`FileFontSource`](../../filefontsource/) la clave de caché es[`CacheKey`](../../filefontsource/cachekey/) propiedad o una ruta de archivo si el[`CacheKey`](../../filefontsource/cachekey/) es **nulo**.

Se recomienda encarecidamente proporcionar las mismas fuentes de fuentes al cargar el caché que en el momento en que se guardó el caché. Cualquier cambio en las fuentes de fuentes (por ejemplo, agregar fuentes nuevas, mover archivos de fuentes o cambiar la clave de caché) puede dar lugar a la fuente inexacta resolviendo por Aspose.Words.

### Ejemplos

Muestra cómo acelerar el proceso de inicialización de caché de fuentes.

```csharp
[Test]
public void LoadFontSearchCache()
{
    const string cacheKey1 = "Arvo";
    const string cacheKey2 = "Arvo-Bold";
    FontSettings parsedFonts = new FontSettings();
    FontSettings loadedCache = new FontSettings();

    parsedFonts.SetFontsSources(new FontSourceBase[]
    {
        new FileFontSource(FontsDir + "Arvo-Regular.ttf", 0, cacheKey1),
        new FileFontSource(FontsDir + "Arvo-Bold.ttf", 0, cacheKey2)
    });

    using (MemoryStream cacheStream = new MemoryStream())
    {
        parsedFonts.SaveSearchCache(cacheStream);
        loadedCache.SetFontsSources(new FontSourceBase[]
        {
            new SearchCacheStream(cacheKey1),                    
            new MemoryFontSource(File.ReadAllBytes(FontsDir + "Arvo-Bold.ttf"), 0, cacheKey2)
        }, cacheStream);
    }

    Assert.AreEqual(parsedFonts.GetFontsSources().Length, loadedCache.GetFontsSources().Length);
}

/// <summary>
/// Cargue los datos de la fuente solo cuando sea necesario en lugar de almacenarlos en la memoria
/// durante toda la vida útil del objeto "FontSettings".
/// </summary>
private class SearchCacheStream : StreamFontSource
{
    public SearchCacheStream(string cacheKey):base(0, cacheKey)
    {
    }

    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Arvo-Regular.ttf");
    }
}
```

### Ver también

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsettings/)
* asamblea [Aspose.Words](../../../)


