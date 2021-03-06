---
title: Item
second_title: Aspose.Words per .NET API Reference
description: Ottiene uno stile per nome o alias.
type: docs
weight: 50
url: /it/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Ottiene uno stile per nome o alias.

```csharp
public Style this[string name] { get; }
```

### Osservazioni

Con distinzione tra maiuscole e minuscole, restituisce null se lo stile con il nome specificato non viene trovato.

Se questo è il nome inglese di uno stile predefinito che non esiste ancora, lo crea automaticamente.

### Esempi

Mostra quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta avverrà automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifica il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;

 // Nella versione corrente di Aspose.Words, la modifica del documento non viene ricostruita automaticamente
// il layout di pagina memorizzato nella cache. Se desideriamo il layout memorizzato nella cache
// per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Guarda anche

* class [Style](../../style)
* class [StyleCollection](../../stylecollection)
* spazio dei nomi [Aspose.Words](../../stylecollection)
* assemblea [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Ottiene uno stile integrato in base al suo identificatore indipendente dalla locale.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| sti | UN[`StyleIdentifier`](../../styleidentifier) valore che specifica lo stile integrato da recuperare. |

### Osservazioni

Quando si accede a uno stile che non esiste ancora, lo crea automaticamente.

### Esempi

Mostra come aggiungere uno stile alla raccolta di stili di un documento.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.DefaultFont.Name = "Courier New";

// Se aggiungiamo uno stile di "StyleType.Paragraph", la raccolta applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Guarda anche

* class [Style](../../style)
* enum [StyleIdentifier](../../styleidentifier)
* class [StyleCollection](../../stylecollection)
* spazio dei nomi [Aspose.Words](../../stylecollection)
* assemblea [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Ottiene uno stile per indice.

```csharp
public Style this[int index] { get; }
```

### Esempi

Mostra come aggiungere uno stile alla raccolta di stili di un documento.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.DefaultFont.Name = "Courier New";

// Se aggiungiamo uno stile di "StyleType.Paragraph", la raccolta applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Guarda anche

* class [Style](../../style)
* class [StyleCollection](../../stylecollection)
* spazio dei nomi [Aspose.Words](../../stylecollection)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
