---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words per .NET
description: Scopri la proprietà DefaultFont di StyleCollection per una formattazione impeccabile del testo dei documenti. Arricchisci i tuoi documenti con uno stile coerente e professionale.
type: docs
weight: 20
url: /it/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Ottiene la formattazione predefinita del testo del documento.

```csharp
public Font DefaultFont { get; }
```

## Osservazioni

Si noti che le impostazioni predefinite per l'intero documento sono state introdotte in Microsoft Word 2007 e sono pienamente supportate nei formati OOXML (Docx) solo. I formati di documento precedenti supportano questa funzionalità in modo limitato e possono essere memorizzati solo i nomi dei font.

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

* class [Font](../../font/)
* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
