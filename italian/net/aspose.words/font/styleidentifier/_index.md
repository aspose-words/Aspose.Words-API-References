---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font StyleIdentifier per gestire facilmente gli stili di carattere nella formattazione. Migliora il tuo design con soluzioni indipendenti dalle impostazioni locali!
type: docs
weight: 420
url: /it/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni locali dello stile di carattere applicato a questa formattazione.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
