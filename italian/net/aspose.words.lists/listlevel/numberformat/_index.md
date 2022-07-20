---
title: NumberFormat
second_title: Aspose.Words per .NET API Reference
description: Restituisce o imposta il formato numerico per il livello di elenco.
type: docs
weight: 70
url: /it/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Restituisce o imposta il formato numerico per il livello di elenco.

```csharp
public string NumberFormat { get; set; }
```

### Osservazioni

Tra i normali caratteri di testo, la stringa può contenere caratteri segnaposto da \x0000 a \x0008 che rappresentano i numeri dai livelli di elenco corrispondenti.

Ad esempio, la stringa "\x0000.\x0001)" genererà un elenco label simile a "1.5)". Il numero "1" è il numero corrente da il 1° livello di elenco, il numero "5" è il numero corrente dal 2° livello di elenco.

Null non è consentito, ma una stringa vuota indica che nessun numero è valido.

### Esempi

Mostra come applicare la formattazione personalizzata dell'elenco ai paragrafi quando si utilizza DocumentBuilder.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizza i primi due livelli di elenco.
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

// Crea paragrafi e applica loro entrambi i livelli di elenco della nostra formattazione personalizzata.
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

Mostra metodi avanzati di personalizzazione delle etichette degli elenchi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Le etichette di livello 1 verranno formattate in base allo stile di paragrafo "Intestazione 1" e avranno un prefisso.
// Sembreranno "Appendice A", "Appendice B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Le etichette di livello 2 visualizzeranno i numeri correnti del primo e del secondo livello di elenco e avranno degli zeri iniziali.
// Se il primo livello di elenco è a 1, le etichette dell'elenco da questi appariranno come "Sezione (1.01)", "Sezione (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Nota che il livello superiore usa la numerazione in lettere maiuscole.
// Possiamo impostare la proprietà "IsLegal" per utilizzare i numeri arabi per i livelli di elenco più alti.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Le etichette di livello 3 saranno numeri romani maiuscoli con un prefisso e un suffisso e ricominceranno a ogni voce di livello 1 dell'elenco.
// Queste etichette di elenco saranno simili a "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Crea in grassetto le etichette di tutti i livelli di elenco.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Applica la formattazione dell'elenco al paragrafo corrente.
builder.ListFormat.List = list;

// Crea voci di elenco che visualizzeranno tutti e tre i livelli di elenco.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Guarda anche

* class [ListLevel](../../listlevel)
* spazio dei nomi [Aspose.Words.Lists](../../listlevel)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
