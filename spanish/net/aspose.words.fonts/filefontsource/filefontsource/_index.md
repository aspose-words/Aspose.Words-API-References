---
title: FileFontSource
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words para .NET
description: Descubre el constructor FileFontSource para una integración fluida de fuentes en tus proyectos. ¡Mejora tu diseño con soluciones de programación fáciles de usar!
type: docs
weight: 10
url: /es/net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(*string*) {#constructor}

Ctor.

```csharp
public FileFontSource(string filePath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| filePath | String | Ruta al archivo de fuente. |

## Ejemplos

Muestra cómo utilizar un archivo de fuente en el sistema de archivos local como fuente de fuente.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Ver también

* class [FileFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)

---

## FileFontSource(*string, int*) {#constructor_1}

Ctor.

```csharp
public FileFontSource(string filePath, int priority)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| filePath | String | Ruta al archivo de fuente. |
| priority | Int32 | Prioridad de la fuente. Ver la[`Priority`](../../fontsourcebase/priority/) Descripción de la propiedad para más información. |

## Ejemplos

Muestra cómo utilizar un archivo de fuente en el sistema de archivos local como fuente de fuente.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Ver también

* class [FileFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)

---

## FileFontSource(*string, int, string*) {#constructor_2}

Ctor.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| filePath | String | Ruta al archivo de fuente. |
| priority | Int32 | Prioridad de la fuente. Ver la[`Priority`](../../fontsourcebase/priority/) Descripción de la propiedad para más información. |
| cacheKey | String | La clave de esta fuente en la caché. Ver[`CacheKey`](../cachekey/) Descripción de la propiedad para más información. |

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

* class [FileFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
