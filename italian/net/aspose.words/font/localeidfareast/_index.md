---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words per .NET
description: Font LocaleIdFarEast proprietà. Ottiene o imposta lidentificatore locale lingua dei caratteri asiatici formattati in C#.
type: docs
weight: 220
url: /it/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Ottiene o imposta l'identificatore locale (lingua) dei caratteri asiatici formattati.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Osservazioni

Per l'elenco degli identificatori locali vedere https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Esempi

Mostra come inserire e formattare il testo in una lingua dell'Estremo Oriente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica le impostazioni dei caratteri che il generatore di documenti applicherà a qualsiasi testo inserito.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nomina gli equivalenti "FarEast" per il nostro carattere e la nostra localizzazione.
// Se il builder inserisce caratteri asiatici con questa configurazione di font, allora ogni esecuzione che contiene
// questi caratteri verranno visualizzati utilizzando il carattere/locale "FarEast" anziché quello predefinito.
// Ciò potrebbe essere utile quando un carattere occidentale non ha rappresentazioni ideali per i caratteri asiatici.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Questo testo verrà visualizzato nel carattere/locale predefinito.
builder.Writeln("Hello world!");

// Poiché questi sono caratteri asiatici, questa esecuzione applicherà i nostri equivalenti font/locali "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
