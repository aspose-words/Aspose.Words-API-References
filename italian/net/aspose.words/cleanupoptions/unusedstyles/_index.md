---
title: CleanupOptions.UnusedStyles
linktitle: UnusedStyles
articleTitle: UnusedStyles
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi documenti con la proprietà UnusedStyles di CleanupOptions, che garantisce la rimozione degli stili inutilizzati per contenuti più puliti e veloci da caricare. Valore predefinito: true.
type: docs
weight: 50
url: /it/net/aspose.words/cleanupoptions/unusedstyles/
---
## CleanupOptions.UnusedStyles property

Specifica se gli stili non utilizzati devono essere rimossi dal documento. Il valore predefinito è`VERO` .

```csharp
public bool UnusedStyles { get; set; }
```

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

* class [CleanupOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
