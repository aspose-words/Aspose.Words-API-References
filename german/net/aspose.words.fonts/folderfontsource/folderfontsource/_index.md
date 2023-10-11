---
title: FolderFontSource.FolderFontSource
second_title: Aspose.Words für .NET-API-Referenz
description: FolderFontSource constructeur. Ctor.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(string, bool) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| folderPath | String | Pfad zum Ordner. |
| scanSubfolders | Boolean | Legt fest, ob Unterordner gescannt werden sollen oder nicht. |

### Beispiele

Zeigt, wie ein lokaler Systemordner, der Schriftarten enthält, als Schriftartenquelle verwendet wird.

```csharp
// Erstellen Sie eine Schriftartenquelle aus einem Ordner, der Schriftartendateien enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Siehe auch

* class [FolderFontSource](../)
* namensraum [Aspose.Words.Fonts](../../folderfontsource/)
* Montage [Aspose.Words](../../../)

---

## FolderFontSource(string, bool, int) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| folderPath | String | Pfad zum Ordner. |
| scanSubfolders | Boolean | Legt fest, ob Unterordner gescannt werden sollen oder nicht. |
| priority | Int32 | Priorität der Schriftartquelle. Siehe die[`Priority`](../../fontsourcebase/priority/) Weitere Informationen finden Sie in der Objektbeschreibung. |

### Beispiele

Zeigt, wie ein lokaler Systemordner, der Schriftarten enthält, als Schriftartenquelle verwendet wird.

```csharp
// Erstellen Sie eine Schriftartenquelle aus einem Ordner, der Schriftartendateien enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Siehe auch

* class [FolderFontSource](../)
* namensraum [Aspose.Words.Fonts](../../folderfontsource/)
* Montage [Aspose.Words](../../../)


