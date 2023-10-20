---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.StyleCollection classe. Una raccolta diStyle oggetti che rappresentano sia gli stili incorporati che quelli definiti dallutente in un documento in C#.
type: docs
weight: 6140
url: /it/net/aspose.words/stylecollection/
---
## StyleCollection class

Una raccolta di[`Style`](../style/) oggetti che rappresentano sia gli stili incorporati che quelli definiti dall'utente in un documento.

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Ottiene il numero di stili nella raccolta. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Ottiene la formattazione del testo predefinita del documento. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Ottiene la formattazione del paragrafo predefinita del documento. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Ottiene il documento del proprietario. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Ottiene uno stile per nome o alias. (3 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Crea un nuovo stile definito dall'utente e lo aggiunge alla raccolta. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Copia uno stile in questa raccolta. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Rimuove tutti gli stili dal pannello Galleria stili veloci. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Ottiene un oggetto enumeratore che enumererà gli stili nell'ordine alfabetico dei relativi nomi. |

## Esempi

Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea uno stile di paragrafo personalizzato.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Crea un elenco e assicurati che i paragrafi che utilizzano questo stile utilizzino questo elenco.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Applica lo stile di paragrafo al paragrafo corrente del generatore di documenti, quindi aggiunge del testo.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Cambia lo stile del generatore di documenti in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Guarda anche

* class [Style](../style/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
