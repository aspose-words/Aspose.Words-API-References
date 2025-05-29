---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words per .NET
description: Scopri come la proprietà Font LocaleId migliora la formattazione del testo gestendo gli identificatori locali per diverse lingue. Migliora il tuo codice oggi stesso!
type: docs
weight: 200
url: /it/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati.

```csharp
public int LocaleId { get; set; }
```

## Osservazioni

Per l'elenco degli identificatori locali, vedere https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Esempi

Mostra come impostare le impostazioni locali del testo che stiamo aggiungendo con un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se impostiamo le impostazioni locali del font su inglese e inseriamo del testo russo,
// il correttore ortografico locale inglese non riconoscerà il testo e lo rileverà come errore di ortografia.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Imposta un'impostazione locale corrispondente per il testo che stiamo per aggiungere per applicare il correttore ortografico appropriato.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
