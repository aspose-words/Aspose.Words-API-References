---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.CleanupOptions per personalizzare la pulizia dei documenti. Migliora il tuo flusso di lavoro con impostazioni personalizzate per documenti più puliti ed efficienti.
type: docs
weight: 400
url: /it/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Consente di specificare le opzioni per la pulizia del documento.

Per saperne di più, visita il[Pulisci un documento](https://docs.aspose.com/words/net/clean-up-a-document/) articolo di documentazione.

```csharp
public class CleanupOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è `falso` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Specifica che non utilizzato[`BuiltIn`](../style/builtin/) gli stili dovrebbero essere rimossi dal documento. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Specifica se l'elenco e le definizioni di elenco non utilizzati devono essere rimossi dal documento. Il valore predefinito è`VERO` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Specifica se gli stili non utilizzati devono essere rimossi dal documento. Il valore predefinito è`VERO` . |

## Esempi

Mostra come rimuovere tutti gli stili personalizzati inutilizzati da un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// In combinazione con gli stili incorporati, il documento ora ha otto stili.
// Uno stile personalizzato viene contrassegnato come "utilizzato" finché è presente del testo all'interno del documento
// formattato in quello stile. Ciò significa che i 4 stili che abbiamo aggiunto sono attualmente inutilizzati.
Assert.AreEqual(8, doc.Styles.Count);

// Applica uno stile di carattere personalizzato e poi uno stile di elenco personalizzato. In questo modo verranno contrassegnati come "usati".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Ora c'è uno stile di carattere inutilizzato e uno stile di elenco inutilizzato.
// Il metodo Cleanup(), se configurato con un oggetto CleanupOptions, può individuare gli stili non utilizzati e rimuoverli.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // La rimozione di ogni nodo a cui è applicato uno stile personalizzato lo contrassegna nuovamente come "non utilizzato".
// Eseguire nuovamente il metodo Cleanup per rimuoverli.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
