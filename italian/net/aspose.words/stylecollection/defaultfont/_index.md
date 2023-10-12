---
title: StyleCollection.DefaultFont
second_title: Aspose.Words per .NET API Reference
description: StyleCollection proprietà. Ottiene la formattazione del testo predefinita del documento.
type: docs
weight: 20
url: /it/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Ottiene la formattazione del testo predefinita del documento.

```csharp
public Font DefaultFont { get; }
```

### Osservazioni

Tieni presente che le impostazioni predefinite a livello di documento sono state introdotte in Microsoft Word 2007 e sono completamente supportate nei formati OOXML (Docx). I formati di documento precedenti hanno un supporto limitato per questa funzionalità ed è possibile memorizzare solo i nomi dei caratteri.

### Esempi

Mostra come aggiungere uno stile alla raccolta di stili di un documento.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.DefaultFont.Name = "Courier New";
// Se aggiungiamo uno stile di "StyleType.Paragraph", la raccolta applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" nella proprietà "ParagraphFormat" dello stile.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Guarda anche

* class [Font](../../font/)
* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../stylecollection/)
* assemblea [Aspose.Words](../../../)


