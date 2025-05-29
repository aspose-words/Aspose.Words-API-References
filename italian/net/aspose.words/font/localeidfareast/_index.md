---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font LocaleIdFarEast per gestire facilmente gli identificatori locali per i caratteri asiatici formattati, migliorando le tue applicazioni multilingue.
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

Per l'elenco degli identificatori locali, vedere https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Esempi

Mostra come inserire e formattare il testo in una lingua dell'Estremo Oriente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare le impostazioni del font che il generatore di documenti applicherà a qualsiasi testo inserito.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Assegna un nome equivalente a "FarEast" al nostro font e alle nostre impostazioni locali.
// Se il builder inserisce caratteri asiatici con questa configurazione del font, ogni esecuzione che contiene
// questi caratteri verranno visualizzati utilizzando il font/impostazioni locali "FarEast" anziché quelle predefinite.
// Questo potrebbe essere utile quando un font occidentale non offre rappresentazioni ideali per i caratteri asiatici.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Questo testo verrà visualizzato con il font/le impostazioni locali predefinite.
builder.Writeln("Hello world!");

// Poiché si tratta di caratteri asiatici, questa esecuzione applicherà i nostri equivalenti font/locali "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
