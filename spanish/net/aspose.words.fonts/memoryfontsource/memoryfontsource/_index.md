---
title: MemoryFontSource.MemoryFontSource
second_title: Referencia de API de Aspose.Words para .NET
description: MemoryFontSource constructor. Director
type: docs
weight: 10
url: /es/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(byte[]) {#constructor}

Director

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuentes binarias. |

### Ejemplos

Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como fuente de fuente.

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
* espacio de nombres [Aspose.Words.Fonts](../../memoryfontsource/)
* asamblea [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int) {#constructor_1}

Director

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuentes binarias. |
| priority | Int32 | Prioridad de fuente de fuente. Ver el[`Priority`](../../fontsourcebase/priority/) descripción de la propiedad para más información. |

### Ejemplos

Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como fuente de fuente.

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
* espacio de nombres [Aspose.Words.Fonts](../../memoryfontsource/)
* asamblea [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int, string) {#constructor_2}

Director

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontData | Byte[] | Datos de fuentes binarias. |
| priority | Int32 | Prioridad de fuente de fuente. Ver el[`Priority`](../../fontsourcebase/priority/) descripción de la propiedad para más información. |
| cacheKey | String | La clave de esta fuente en el caché. Ver[`CacheKey`](../cachekey/) descripción de la propiedad para más información. |

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

* class [MemoryFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../memoryfontsource/)
* asamblea [Aspose.Words](../../../)


