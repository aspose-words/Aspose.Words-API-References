---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words für .NET
description: Entdecken Sie verfügbare Schriftarten mit der GetAvailableFonts-Methode von FontSourceBase. Werten Sie Ihre Projekte mit einer vielfältigen Auswahl hochwertiger Schriften auf!
type: docs
weight: 40
url: /de/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

## Beispiele

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```csharp
// Konfigurieren Sie Aspose.Words so, dass Schriftarten aus einem benutzerdefinierten Ordner bezogen werden, und drucken Sie dann alle verfügbaren Schriftarten.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Siehe auch

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
