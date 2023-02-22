---
title: Font.NameFarEast
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Restituisce o imposta un nome di carattere dellAsia orientale.
type: docs
weight: 260
url: /it/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Restituisce o imposta un nome di carattere dell'Asia orientale.

```csharp
public string NameFarEast { get; set; }
```

### Esempi

Mostra come inserire e formattare il testo in una lingua dell'Estremo Oriente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica le impostazioni del carattere che il generatore di documenti applicherà a qualsiasi testo inserito.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nome equivalenti "FarEast" per il nostro carattere e locale.
// Se il builder inserisce caratteri asiatici con questa configurazione di Font, esegui ogni che contiene
// questi caratteri li visualizzeranno usando il font/locale "FarEast" invece del default.
// Questo potrebbe essere utile quando un font occidentale non ha rappresentazioni ideali per i caratteri asiatici.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Questo testo verrà visualizzato nel carattere/locale predefinito.
builder.Writeln("Hello world!");

// Poiché si tratta di caratteri asiatici, questa esecuzione applicherà i nostri equivalenti font/locali "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Guarda anche

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


