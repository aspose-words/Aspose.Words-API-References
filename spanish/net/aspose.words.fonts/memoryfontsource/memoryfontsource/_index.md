---
title: MemoryFontSource
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words para .NET
description: Descubre MemoryFontSource, un potente constructor para una gestión de fuentes fluida en tus proyectos. ¡Mejora tu diseño con facilidad y eficiencia!
type: docs
weight: 10
url: /es/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(*byte[]*) {#constructor}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuente binaria. |

## Ejemplos

Muestra cómo utilizar una matriz de bytes con datos de un archivo de fuente como fuente.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ver también

* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int*) {#constructor_1}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuente binaria. |
| priority | Int32 | Prioridad de la fuente. Ver la[`Priority`](../../fontsourcebase/priority/) Descripción de la propiedad para más información. |

## Ejemplos

Muestra cómo utilizar una matriz de bytes con datos de un archivo de fuente como fuente.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ver también

* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int, string*) {#constructor_2}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuente binaria. |
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

* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
