---
title: ListLevel.LinkedStyle
second_title: Aspose.Words per .NET API Reference
description: ListLevel proprietà. Ottiene o imposta lo stile di paragrafo collegato a questo livello di elenco.
type: docs
weight: 60
url: /it/net/aspose.words.lists/listlevel/linkedstyle/
---
## ListLevel.LinkedStyle property

Ottiene o imposta lo stile di paragrafo collegato a questo livello di elenco.

```csharp
public Style LinkedStyle { get; set; }
```

### Osservazioni

Questa proprietà è`nullo` quando il livello dell'elenco non è collegato a uno stile di paragrafo. Questa proprietà può essere impostata su`nullo`.

### Esempi

Mostra modalità avanzate per personalizzare le etichette degli elenchi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Le etichette di livello 1 verranno formattate secondo lo stile di paragrafo "Intestazione 1" e avranno un prefisso.
// Appariranno come "Appendice A", "Appendice B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Le etichette del livello 2 visualizzeranno i numeri correnti del primo e del secondo livello dell'elenco e avranno zeri iniziali.
// Se il primo livello dell'elenco è 1, le etichette dell'elenco saranno simili a "Sezione (1.01)", "Sezione (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Nota che il livello superiore utilizza la numerazione con lettere maiuscole.
// Possiamo impostare la proprietà "IsLegal" per utilizzare i numeri arabi per i livelli di elenco più alti.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Le etichette di livello 3 saranno costituite da numeri romani maiuscoli con un prefisso e un suffisso e ricominceranno da ogni elemento dell'elenco di livello 1.
// Queste etichette dell'elenco saranno simili a "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Rende in grassetto le etichette di tutti i livelli dell'elenco.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Applica la formattazione dell'elenco al paragrafo corrente.
builder.ListFormat.List = list;

// Crea elementi dell'elenco che visualizzeranno tutti e tre i livelli dell'elenco.
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

* class [Style](../../../aspose.words/style/)
* class [ListLevel](../)
* spazio dei nomi [Aspose.Words.Lists](../../listlevel/)
* assemblea [Aspose.Words](../../../)


