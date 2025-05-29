---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà StyleCollection Count per recuperare facilmente il numero totale di stili nella tua collezione, per una migliore organizzazione e gestione.
type: docs
weight: 10
url: /it/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Ottiene il numero di stili nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come aggiungere uno stile alla raccolta di stili di un documento.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.DefaultFont.Name = "Courier New";
// Se aggiungiamo uno stile di "StyleType.Paragraph", la raccolta applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Aggiungi uno stile e verifica che abbia le impostazioni predefinite.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Guarda anche

* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
