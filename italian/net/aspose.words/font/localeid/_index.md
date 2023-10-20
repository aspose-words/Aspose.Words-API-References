---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words per .NET
description: Font LocaleId proprietà. Ottiene o imposta lidentificatore locale lingua dei caratteri formattati in C#.
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

Per l'elenco degli identificatori locali vedere https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Esempi

Mostra come impostare la lingua del testo che stiamo aggiungendo con un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se impostiamo la locale del carattere su inglese e inseriamo del testo in russo,
// il controllo ortografico locale inglese non riconoscerà il testo e lo rileverà come un errore di ortografia.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Imposta una lingua corrispondente per il testo che stiamo per aggiungere per applicare il correttore ortografico appropriato.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
