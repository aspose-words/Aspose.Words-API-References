---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words per .NET
description: Scopri il metodo CompositeNode GetText per recuperare in modo efficiente il testo dai nodi e dai loro elementi figlio, migliorando le tue capacità di elaborazione dei dati.
type: docs
weight: 130
url: /it/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Ottiene il testo di questo nodo e di tutti i suoi figli.

```csharp
public override string GetText()
```

## Osservazioni

La stringa restituita include tutti i caratteri di controllo e speciali come descritto in[`ControlChar`](../../controlchar/).

## Esempi

Mostra la differenza tra la chiamata dei metodi GetText e ToString su un nodo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText recupererà il testo visibile, nonché i codici di campo e i caratteri speciali.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString ci fornirà l'aspetto del documento se salvato in un formato di salvataggio trasmesso.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Mostra come visualizzare tutti i paragrafi di un documento che sono elementi di elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Guarda anche

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
