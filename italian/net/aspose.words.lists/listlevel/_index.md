---
title: Class ListLevel
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Lists.ListLevel classe. Definisce la formattazione per un livello di elenco.
type: docs
weight: 3500
url: /it/net/aspose.words.lists/listlevel/
---
## ListLevel class

Definisce la formattazione per un livello di elenco.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class ListLevel
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Ottiene o imposta la giustificazione del numero effettivo della voce dell'elenco. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Ottiene il formato di stile numero personalizzato per questo livello di elenco. Ad esempio: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Specifica la formattazione dei caratteri utilizzata per l'etichetta dell'elenco. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Restituisce i dati dell'immagine della forma del punto elenco dell'immagine per il livello dell'elenco corrente. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Vero se il livello trasforma tutti i numeri ereditati in arabo, falso se ne preserva lo stile numerico. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Ottiene o imposta lo stile di paragrafo collegato a questo livello di elenco. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Restituisce o imposta il formato numerico per il livello dell'elenco. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Restituisce o imposta la posizione (in punti) del numero o del punto elenco per il livello dell'elenco. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Restituisce o imposta lo stile del numero per questo livello di elenco. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Imposta o restituisce il livello di elenco che deve essere visualizzato prima che il livello di elenco specificato riprenda la numerazione. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Restituisce o imposta il numero iniziale per questo livello di elenco. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Restituisce o imposta la posizione della tabulazione (in punti) per il livello dell'elenco. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Restituisce o imposta la posizione (in punti) per la seconda riga di testo a capo per il livello di elenco. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Restituisce o imposta il carattere inserito dopo il numero per il livello della lista. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Crea la forma di un punto elenco per il livello di elenco corrente. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Elimina l'immagine puntata per il livello di elenco corrente. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(ListLevel) | Confronta con il ListLevel specificato. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Calcola il codice hash per questo oggetto. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(int, NumberStyle, string) | Riporta la rappresentazione in stringa del file`ListLevel`oggetto per l'indice specificato dell'elemento dell'elenco. I parametri specificano il[`NumberStyle`](../../aspose.words/numberstyle/) e un formato opzionale string utilizzato quandoCustom è specificato. |

### Osservazioni

Non crei oggetti di questa classe. Gli oggetti a livello di elenco vengono creati automaticamente quando viene creato un elenco. Tu accedi`ListLevel` oggetti tramite the [`ListLevelCollection`](../listlevelcollection/) collezione.

Utilizza le proprietà di`ListLevel` per specificare la formattazione dell'elenco per i singoli livelli di elenco.

### Esempi

Mostra come applicare la formattazione dell'elenco personalizzato ai paragrafi quando si utilizza DocumentBuilder.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Crea un elenco da un modello Microsoft Word e personalizza i primi due livelli dell'elenco.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Questo valore NumberFormat creerà simboli di elenchi puntati a forma di stella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Crea paragrafi e applica loro entrambi i livelli di elenco della nostra formattazione di elenco personalizzata.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)


