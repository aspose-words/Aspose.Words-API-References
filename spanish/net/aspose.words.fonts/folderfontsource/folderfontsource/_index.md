---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words para .NET
description: Descubre el constructor FolderFontSource para una gestión de fuentes fluida. ¡Mejora tus proyectos web con una búsqueda eficiente de fuentes hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| folderPath | String | Ruta a la carpeta. |
| scanSubfolders | Boolean | Determina si se deben escanear o no las subcarpetas. |

## Ejemplos

Muestra cómo utilizar una carpeta de sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuente.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ver también

* class [FolderFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| folderPath | String | Ruta a la carpeta. |
| scanSubfolders | Boolean | Determina si se deben escanear o no las subcarpetas. |
| priority | Int32 | Prioridad de la fuente. Ver la[`Priority`](../../fontsourcebase/priority/) Descripción de la propiedad para más información. |

## Ejemplos

Muestra cómo utilizar una carpeta de sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuente.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ver también

* class [FolderFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
