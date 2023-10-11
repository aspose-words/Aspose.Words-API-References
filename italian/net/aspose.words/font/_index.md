---
title: Class Font
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Font classe. Contiene gli attributi del carattere nome del carattere dimensione del carattere colore e così via per un oggetto.
type: docs
weight: 2830
url: /it/net/aspose.words/font/
---
## Font class

Contiene gli attributi del carattere (nome del carattere, dimensione del carattere, colore e così via) per un oggetto.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class Font
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllCaps](../../aspose.words/font/allcaps/) { get; set; } | Vero se il carattere è formattato con tutte lettere maiuscole. |
| [AutoColor](../../aspose.words/font/autocolor/) { get; } | Restituisce il colore calcolato attuale del testo (bianco o nero) da utilizzare per 'colore automatico'. Se il colore non è 'auto' restituisce[`Color`](./color/) . |
| [Bidi](../../aspose.words/font/bidi/) { get; set; } | Specifica se il contenuto di questa esecuzione dovrà avere caratteristiche da destra a sinistra. |
| [Bold](../../aspose.words/font/bold/) { get; set; } | Vero se il carattere è formattato in grassetto. |
| [BoldBi](../../aspose.words/font/boldbi/) { get; set; } | Vero se il testo da destra a sinistra è formattato in grassetto. |
| [Border](../../aspose.words/font/border/) { get; } | Restituisce a[`Border`](../border/) oggetto che specifica il bordo per il font. |
| [Color](../../aspose.words/font/color/) { get; set; } | Ottiene o imposta il colore del carattere. |
| [ComplexScript](../../aspose.words/font/complexscript/) { get; set; } | Specifica se il contenuto di questa esecuzione deve essere trattato come testo di script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione per questa esecuzione. |
| [DoubleStrikeThrough](../../aspose.words/font/doublestrikethrough/) { get; set; } | Vero se il carattere è formattato come testo barrato doppio. |
| [Emboss](../../aspose.words/font/emboss/) { get; set; } | Vero se il carattere è formattato in rilievo. |
| [EmphasisMark](../../aspose.words/font/emphasismark/) { get; set; } | Ottiene o imposta il segno di enfasi applicato a questa formattazione. |
| [Engrave](../../aspose.words/font/engrave/) { get; set; } | Vero se il carattere è formattato come inciso. |
| [Fill](../../aspose.words/font/fill/) { get; } | Ottiene la formattazione di riempimento per il file`Font` . |
| [Hidden](../../aspose.words/font/hidden/) { get; set; } | Vero se il carattere è formattato come testo nascosto. |
| [HighlightColor](../../aspose.words/font/highlightcolor/) { get; set; } | Ottiene o imposta il colore dell'evidenziazione (marcatore). |
| [Italic](../../aspose.words/font/italic/) { get; set; } | Vero se il carattere è formattato come corsivo. |
| [ItalicBi](../../aspose.words/font/italicbi/) { get; set; } | Vero se il testo da destra a sinistra è formattato in corsivo. |
| [Kerning](../../aspose.words/font/kerning/) { get; set; } | Ottiene o imposta la dimensione del carattere a partire dalla quale inizia la crenatura. |
| [LineSpacing](../../aspose.words/font/linespacing/) { get; } | Restituisce l'interlinea di questo carattere (in punti). |
| [LocaleId](../../aspose.words/font/localeid/) { get; set; } | Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati. |
| [LocaleIdBi](../../aspose.words/font/localeidbi/) { get; set; } | Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati da destra a sinistra. |
| [LocaleIdFarEast](../../aspose.words/font/localeidfareast/) { get; set; } | Ottiene o imposta l'identificatore locale (lingua) dei caratteri asiatici formattati. |
| [Name](../../aspose.words/font/name/) { get; set; } | Ottiene o imposta il nome del carattere. |
| [NameAscii](../../aspose.words/font/nameascii/) { get; set; } | Restituisce o imposta il carattere utilizzato per il testo latino (caratteri con codici carattere da 0 (zero) a 127). |
| [NameBi](../../aspose.words/font/namebi/) { get; set; } | Restituisce o imposta il nome del carattere in un documento in lingua da destra a sinistra. |
| [NameFarEast](../../aspose.words/font/namefareast/) { get; set; } | Restituisce o imposta il nome di un font dell'Asia orientale. |
| [NameOther](../../aspose.words/font/nameother/) { get; set; } | Restituisce o imposta il carattere utilizzato per i caratteri con codici carattere da 128 a 255. |
| [NoProofing](../../aspose.words/font/noproofing/) { get; set; } | Vero quando i caratteri formattati non devono essere sottoposti al controllo ortografico. |
| [Outline](../../aspose.words/font/outline/) { get; set; } | Vero se il carattere è formattato come contorno. |
| [Position](../../aspose.words/font/position/) { get; set; } | Ottiene o imposta la posizione del testo (in punti) rispetto alla linea di base. Un numero positivo solleva il testo e un numero negativo lo abbassa. |
| [Scaling](../../aspose.words/font/scaling/) { get; set; } | Ottiene o imposta il ridimensionamento della larghezza dei caratteri in percentuale. |
| [Shading](../../aspose.words/font/shading/) { get; } | Restituisce a[`Shading`](../shading/) oggetto che fa riferimento alla formattazione dell'ombreggiatura per il font. |
| [Shadow](../../aspose.words/font/shadow/) { get; set; } | Vero se il carattere è formattato come ombreggiato. |
| [Size](../../aspose.words/font/size/) { get; set; } | Ottiene o imposta la dimensione del carattere in punti. |
| [SizeBi](../../aspose.words/font/sizebi/) { get; set; } | Ottiene o imposta la dimensione del carattere in punti utilizzati in un documento da destra a sinistra. |
| [SmallCaps](../../aspose.words/font/smallcaps/) { get; set; } | Vero se il carattere è formattato come lettere maiuscole. |
| [SnapToGrid](../../aspose.words/font/snaptogrid/) { get; set; } | Specifica se il carattere corrente deve utilizzare i caratteri della griglia del documento per le impostazioni di riga durante il layout. |
| [Spacing](../../aspose.words/font/spacing/) { get; set; } | Restituisce o imposta la spaziatura (in punti) tra i caratteri . |
| [StrikeThrough](../../aspose.words/font/strikethrough/) { get; set; } | Vero se il carattere è formattato come testo barrato. |
| [Style](../../aspose.words/font/style/) { get; set; } | Ottiene o imposta lo stile di carattere applicato a questa formattazione. |
| [StyleIdentifier](../../aspose.words/font/styleidentifier/) { get; set; } | Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni internazionali dello stile di carattere applicato a questa formattazione. |
| [StyleName](../../aspose.words/font/stylename/) { get; set; } | Ottiene o imposta il nome dello stile di carattere applicato a questa formattazione. |
| [Subscript](../../aspose.words/font/subscript/) { get; set; } | Vero se il carattere è formattato come pedice. |
| [Superscript](../../aspose.words/font/superscript/) { get; set; } | Vero se il carattere è formattato come apice. |
| [TextEffect](../../aspose.words/font/texteffect/) { get; set; } | Ottiene o imposta l'effetto di animazione del carattere. |
| [ThemeColor](../../aspose.words/font/themecolor/) { get; set; } | Ottiene o imposta il colore del tema nella combinazione di colori applicata associata a questo`Font` oggetto. |
| [ThemeFont](../../aspose.words/font/themefont/) { get; set; } | Ottiene o imposta il carattere del tema nello schema di caratteri applicato associato a questo`Font` oggetto. |
| [ThemeFontAscii](../../aspose.words/font/themefontascii/) { get; set; } | Ottiene o imposta il carattere del tema utilizzato per il testo latino (caratteri con codici carattere da 0 (zero) a 127) nello schema di caratteri applicato associato a questo`Font` oggetto. |
| [ThemeFontBi](../../aspose.words/font/themefontbi/) { get; set; } | Ottiene o imposta il carattere del tema nello schema di caratteri applicato associato a questo`Font` object in un documento in lingua da destra a sinistra. |
| [ThemeFontFarEast](../../aspose.words/font/themefontfareast/) { get; set; } | Ottiene o imposta il carattere del tema dell'Asia orientale nello schema di caratteri applicato associato a questo`Font` oggetto. |
| [ThemeFontOther](../../aspose.words/font/themefontother/) { get; set; } | Ottiene o imposta il carattere del tema utilizzato per i caratteri con codici carattere da 128 a 255 nello schema di caratteri applicato associato a questo`Font` oggetto. |
| [TintAndShade](../../aspose.words/font/tintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce un colore. |
| [Underline](../../aspose.words/font/underline/) { get; set; } | Ottiene o imposta il tipo di sottolineatura applicata al carattere. |
| [UnderlineColor](../../aspose.words/font/underlinecolor/) { get; set; } | Ottiene o imposta il colore della sottolineatura applicata al carattere. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/font/clearformatting/)() | Ripristina la formattazione predefinita dei caratteri. |
| [HasDmlEffect](../../aspose.words/font/hasdmleffect/)(TextDmlEffect) | Controlla se viene applicato un particolare effetto di testo DrawingML. |

### Osservazioni

Non crei istanze di`Font`classe direttamente. Usa solo `Font` per accedere alle proprietà dei caratteri dei vari oggetti come[`Run`](../run/) , [`Paragraph`](../paragraph/) ,[`Style`](../style/) ,[`DocumentBuilder`](../documentbuilder/).

### Esempi

Mostra come formattare una sequenza di testo utilizzando la relativa proprietà font.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Mostra come inserire una stringa circondata da un bordo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


