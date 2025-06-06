---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font StyleName, gestisci facilmente gli stili di carattere per una formattazione del testo migliorata e maggiore flessibilità di progettazione nei tuoi progetti.
type: docs
weight: 430
url: /it/net/aspose.words/font/stylename/
---
## Font.StyleName property

Ottiene o imposta il nome dello stile di carattere applicato a questa formattazione.

```csharp
public string StyleName { get; set; }
```

## Esempi

Mostra come modificare lo stile del testo esistente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per fare riferimento agli stili.
// 1 - Utilizzando il nome dello stile:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Utilizzo di un identificatore di stile incorporato:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Converti tutti gli usi di uno stile in un altro,
// utilizzando i metodi sopra indicati per fare riferimento a stili vecchi e nuovi.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
