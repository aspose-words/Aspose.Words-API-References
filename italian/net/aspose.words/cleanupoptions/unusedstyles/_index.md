---
title: CleanupOptions.UnusedStyles
second_title: Aspose.Words per .NET API Reference
description: CleanupOptions proprietà. Specifica se gli stili inutilizzati devono essere rimossi dal documento. Il valore predefinito èVERO .
type: docs
weight: 50
url: /it/net/aspose.words/cleanupoptions/unusedstyles/
---
## CleanupOptions.UnusedStyles property

Specifica se gli stili inutilizzati devono essere rimossi dal documento. Il valore predefinito è`VERO` .

```csharp
public bool UnusedStyles { get; set; }
```

### Esempi

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// In combinazione con gli stili incorporati, il documento ora ha otto stili.
// Uno stile personalizzato è contrassegnato come "usato" mentre è presente testo nel documento
// formattato in quello stile. Ciò significa che i 4 stili che abbiamo aggiunto sono attualmente inutilizzati.
Assert.AreEqual(8, doc.Styles.Count);

// Applica uno stile di carattere personalizzato e quindi uno stile di elenco personalizzato. Ciò li contrassegnerà come "usati".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Ora c'è uno stile di carattere inutilizzato e uno stile di elenco inutilizzato.
// Il metodo Cleanup(), se configurato con un oggetto CleanupOptions, può prendere di mira gli stili inutilizzati e rimuoverli.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // La rimozione di ogni nodo a cui viene applicato uno stile personalizzato lo contrassegna nuovamente come "inutilizzato".
// Eseguire nuovamente il metodo Cleanup per rimuoverli.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Guarda anche

* class [CleanupOptions](../)
* spazio dei nomi [Aspose.Words](../../cleanupoptions/)
* assemblea [Aspose.Words](../../../)


