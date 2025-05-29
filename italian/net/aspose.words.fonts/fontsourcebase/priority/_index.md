---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontSourceBase Priority per ottimizzare il sourcing dei tuoi font. Migliora le prestazioni e l'esperienza utente senza sforzo!
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Restituisce la priorità della sorgente del font.

```csharp
public int Priority { get; }
```

## Osservazioni

Questo valore viene utilizzato quando sono presenti font con lo stesso nome di famiglia e stile in diverse origini font. In questo caso Aspose.Words seleziona il font dall'origine con il valore di priorità più alto.

Il valore predefinito è 0.

## Esempi

Mostra come utilizzare un file di font nel file system locale come origine del font.

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
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
