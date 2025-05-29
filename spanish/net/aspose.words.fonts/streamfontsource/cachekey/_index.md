---
title: StreamFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words para .NET
description: Descubra la propiedad CacheKey de StreamFontSource, optimice la gestión de sus fuentes con un almacenamiento en caché eficiente para tiempos de carga más rápidos y un rendimiento mejorado.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/streamfontsource/cachekey/
---
## StreamFontSource.CacheKey property

La clave de esta fuente en la caché.

```csharp
public string CacheKey { get; }
```

## Observaciones

Esta clave se utiliza para identificar el elemento de caché al guardar o cargar el caché de búsqueda de fuentes con [`SaveSearchCache`](../../fontsettings/savesearchcache/) y[`SetFontsSources`](../../fontsettings/setfontssources/) métodos.

## Ejemplos

Muestra cómo acelerar el proceso de inicialización de la caché de fuentes.

```csharp
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

* class [StreamFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
