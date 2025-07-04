---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words for .NET
description: Discover the FolderFontSource constructor for seamless font management. Enhance your web projects with efficient font sourcing today!
type: docs
weight: 10
url: /net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | String | Path to folder. |
| scanSubfolders | Boolean | Determines whether or not to scan subfolders. |

## Examples

Shows how to use a local system folder which contains fonts as a font source.

```csharp
// Create a font source from a folder that contains font files.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.That(folderFontSource.FolderPath, Is.EqualTo(FontsDir));
Assert.That(folderFontSource.ScanSubfolders, Is.EqualTo(false));
Assert.That(folderFontSource.Type, Is.EqualTo(FontSourceType.FontsFolder));
Assert.That(folderFontSource.Priority, Is.EqualTo(1));
```

### See Also

* class [FolderFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | String | Path to folder. |
| scanSubfolders | Boolean | Determines whether or not to scan subfolders. |
| priority | Int32 | Font source priority. See the [`Priority`](../../fontsourcebase/priority/) property description for more information. |

## Examples

Shows how to use a local system folder which contains fonts as a font source.

```csharp
// Create a font source from a folder that contains font files.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.That(folderFontSource.FolderPath, Is.EqualTo(FontsDir));
Assert.That(folderFontSource.ScanSubfolders, Is.EqualTo(false));
Assert.That(folderFontSource.Type, Is.EqualTo(FontSourceType.FontsFolder));
Assert.That(folderFontSource.Priority, Is.EqualTo(1));
```

### See Also

* class [FolderFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
