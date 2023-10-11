---
title: Class Style
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Style classe. Rappresenta un singolo stile integrato o definito dallutente.
type: docs
weight: 6130
url: /it/net/aspose.words/style/
---
## Style class

Rappresenta un singolo stile integrato o definito dall'utente.

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public class Style
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Ottiene tutti gli alias di questo stile. Se lo stile non ha alias, viene restituito un array di stringhe vuoto. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Specifica se questo stile viene ridefinito automaticamente in base al valore appropriato. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Ottiene/imposta il nome dello stile su cui è basato questo stile. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Vero se questo stile è uno degli stili incorporati in MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Ottiene il documento del proprietario. |
| [Font](../../aspose.words/style/font/) { get; } | Ottiene la formattazione dei caratteri dello stile. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Vero quando lo stile è uno degli stili di intestazione integrati. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Specifica se questo stile viene mostrato nella raccolta Stile veloce all'interno dell'interfaccia utente di MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Ottiene il nome del file`Style` legato a questo. Restituisce una stringa vuota se non ci sono stili collegati. |
| [List](../../aspose.words/style/list/) { get; } | Ottiene l'elenco che definisce la formattazione di questo stile di elenco. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo. |
| [Locked](../../aspose.words/style/locked/) { get; set; } |  |
| [Name](../../aspose.words/style/name/) { get; set; } | Ottiene o imposta il nome dello stile. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Ottiene/imposta il nome dello stile da applicare automaticamente ad un nuovo paragrafo inserito dopo un paragrafo formattato con lo stile specificato. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Ottiene la formattazione del paragrafo dello stile. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Ottiene l'identificatore di stile indipendente dalle impostazioni internazionali per uno stile integrato. |
| [Styles](../../aspose.words/style/styles/) { get; } | Ottiene la raccolta di stili a cui appartiene questo stile. |
| [Type](../../aspose.words/style/type/) { get; } | Ottiene il tipo di stile (paragrafo o carattere). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(Style) | Confronta con lo stile specificato. Gli stili Istd vengono confrontati solo per gli stili incorporati. Gli stili predefiniti non sono inclusi nel confronto. Lo stile di base, lo stile collegato e lo stile del paragrafo successivo vengono confrontati ricorsivamente. |
| [Remove](../../aspose.words/style/remove/)() | Rimuove lo stile specificato dal documento. |

### Esempi

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

Mostra come creare e applicare uno stile personalizzato.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Ridefinisce automaticamente lo stile.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Applica uno degli stili del documento al paragrafo che il generatore di documenti sta creando.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Rimuove il nostro stile personalizzato dalla raccolta di stili del documento.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Qualsiasi testo che utilizzava uno stile rimosso ripristina la formattazione predefinita.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


