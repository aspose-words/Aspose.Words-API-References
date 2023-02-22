---
title: Class TableStyle
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TableStyle classe. Rappresenta uno stile di tabella.
type: docs
weight: 5920
url: /it/net/aspose.words/tablestyle/
---
## TableStyle class

Rappresenta uno stile di tabella.

```csharp
public class TableStyle : Style
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Ottiene tutti gli alias di questo stile. Se lo stile non ha alias, viene restituito un array di stringhe vuoto. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | Specifica l'allineamento per lo stile della tabella. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | Ottiene o imposta un flag che indica se il testo in una riga di tabella può essere suddiviso in un'interruzione di pagina. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Ottiene/imposta il nome dello stile su cui si basa questo stile. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | Ottiene o imposta se questo è uno stile per una tabella da destra a sinistra. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | Ottiene la raccolta dei bordi delle celle predefiniti per lo stile. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle della tabella. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Vero se questo stile è uno degli stili incorporati in MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) tra le celle. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | Ottiene o imposta un numero di colonne da includere nella fascia quando lo stile specifica la fascia delle colonne pari/dispari. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | Raccolta di stili condizionali che possono essere definiti per questo stile di tabella. |
| [Document](../../aspose.words/style/document/) { get; } | Ottiene il documento proprietario. |
| [Font](../../aspose.words/style/font/) { get; } | Ottiene la formattazione dei caratteri dello stile. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Vero quando lo stile è uno degli stili di intestazione incorporati. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Specifica se questo stile viene visualizzato nella raccolta Stili rapidi all'interno dell'interfaccia utente di MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | Ottiene o imposta il valore che rappresenta il rientro sinistro di una tabella. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Ottiene il nome dello stile collegato a questo. Restituisce una stringa vuota se nessuno stile è collegato. |
| [List](../../aspose.words/style/list/) { get; } | Ottiene l'elenco che definisce la formattazione di questo stile di elenco. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo. |
| [Name](../../aspose.words/style/name/) { get; set; } | Ottiene o imposta il nome dello stile. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Ottiene/imposta il nome dello stile da applicare automaticamente a un nuovo paragrafo inserito dopo un paragrafo formattato con lo stile specificato. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Ottiene la formattazione del paragrafo dello stile. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle della tabella. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | Ottiene o imposta un numero di righe da includere nella fascia quando lo stile specifica la fascia di riga pari/dispari. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | Ottiene a[`Shading`](../shading/) oggetto che fa riferimento alla formattazione dell'ombreggiatura per le celle della tabella. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Ottiene l'identificatore di stile indipendente dalla locale per uno stile integrato. |
| [Styles](../../aspose.words/style/styles/) { get; } | Ottiene la raccolta di stili a cui appartiene questo stile. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella. |
| [Type](../../aspose.words/style/type/) { get; } | Ottiene il tipo di stile (paragrafo o carattere). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | Specifica l'allineamento verticale per le celle. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(Style) | Confronta con lo stile specificato. Gli stili Istd vengono confrontati solo per gli stili incorporati. Gli stili predefiniti non sono inclusi nel confronto. Lo stile di base, lo stile collegato e lo stile di paragrafo successivo vengono confrontati in modo ricorsivo. |
| [Remove](../../aspose.words/style/remove/)() | Rimuove lo stile specificato dal documento. |

### Esempi

Mostra come creare impostazioni di stile personalizzate per la tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// L'impostazione delle proprietà di stile di una tabella può influire sulle proprietà della tabella stessa.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Guarda anche

* class [Style](../style/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


