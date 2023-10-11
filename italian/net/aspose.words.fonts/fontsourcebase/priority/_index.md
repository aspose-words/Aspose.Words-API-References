---
title: FontSourceBase.Priority
second_title: Aspose.Words per .NET API Reference
description: FontSourceBase proprietà. Restituisce la priorità della fonte del carattere.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Restituisce la priorità della fonte del carattere.

```csharp
public int Priority { get; }
```

### Osservazioni

Questo valore viene utilizzato quando sono presenti caratteri con lo stesso nome di famiglia e stile in diverse origini di caratteri. In questo caso Aspose.Words seleziona il carattere dall'origine con il valore di priorità più alto.

Il valore predefinito è 0.

### Esempi

Mostra come utilizzare un file di font nel file system locale come origine di font.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Guarda anche

* class [FontSourceBase](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontsourcebase/)
* assemblea [Aspose.Words](../../../)


