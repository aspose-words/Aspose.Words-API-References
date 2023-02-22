---
title: Document.Cleanup
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Pulisce gli stili e gli elenchi inutilizzati dal documento.
type: docs
weight: 520
url: /it/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Pulisce gli stili e gli elenchi inutilizzati dal documento.

```csharp
public void Cleanup()
```

### Esempi

Mostra come rimuovere gli stili personalizzati non utilizzati da un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combinato con gli stili incorporati, il documento ora ha otto stili.
// Uno stile personalizzato conta come "usato" quando applicato a una parte del documento,
// il che significa che i quattro stili che abbiamo aggiunto non sono attualmente utilizzati.
Assert.AreEqual(8, doc.Styles.Count);

// Applica uno stile di carattere personalizzato, quindi uno stile di elenco personalizzato. In questo modo gli stili verranno contrassegnati come "usati".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Rimuove ogni nodo a cui viene applicato uno stile personalizzato e lo contrassegna nuovamente come "non utilizzato".
// Esegui nuovamente il metodo Cleanup per rimuoverli.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Cleanup(CleanupOptions) {#cleanup_1}

Pulisce gli stili e gli elenchi inutilizzati dal documento a seconda del dato[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

### Esempi

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combinato con gli stili incorporati, il documento ora ha otto stili.
// Uno stile personalizzato è contrassegnato come "usato" mentre è presente del testo all'interno del documento
// formattato in quello stile. Ciò significa che i 4 stili che abbiamo aggiunto non sono attualmente utilizzati.
Assert.AreEqual(8, doc.Styles.Count);

// Applica uno stile di carattere personalizzato, quindi uno stile di elenco personalizzato. In questo modo verranno contrassegnati come "usati".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Ora c'è uno stile di carattere inutilizzato e uno stile di elenco inutilizzato.
// Il metodo Cleanup(), se configurato con un oggetto CleanupOptions, può indirizzare gli stili inutilizzati e rimuoverli.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

// Rimuove ogni nodo a cui viene applicato uno stile personalizzato e lo contrassegna nuovamente come "non utilizzato". 
// Esegui nuovamente il metodo Cleanup per rimuoverli.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Guarda anche

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


