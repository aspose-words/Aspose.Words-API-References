---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words per .NET
description: Font NameFarEast proprietà. Restituisce o imposta il nome di un font dellAsia orientale in C#.
type: docs
weight: 260
url: /it/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Restituisce o imposta il nome di un font dell'Asia orientale.

```csharp
public string NameFarEast { get; set; }
```

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

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
