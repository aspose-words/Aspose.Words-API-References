---
title: ListTemplate
second_title: Aspose.Words per .NET API Reference
description: Specifica uno dei formati di elenco predefiniti disponibili in Microsoft Word.
type: docs
weight: 3330
url: /it/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Specifica uno dei formati di elenco predefiniti disponibili in Microsoft Word.

```csharp
public enum ListTemplate
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| BulletDefault | `0` | Elenco puntato predefinito con 9 livelli. Il punto elenco del primo livello è un disco, il punto elenco del secondo livello è un cerchio, il punto elenco del terzo livello è un quadrato. Quindi la formattazione si ripete per i livelli rimanenti. |
| BulletDisk | `0` | Uguale a BulletDefault. |
| BulletCircle | `1` | Il proiettile del primo livello è un cerchio. I livelli rimanenti sono gli stessi di BulletDefault. |
| BulletSquare | `2` | Il proiettile del primo livello è un quadrato. I livelli rimanenti sono gli stessi di BulletDefault. |
| BulletDiamonds | `3` | Il proiettile del primo livello è un personaggio Wingding a 4 diamanti. I livelli rimanenti sono gli stessi di BulletDefault. |
| BulletArrowHead | `4` | Il proiettile del primo livello è un personaggio Wingding con la punta di una freccia. I livelli rimanenti sono gli stessi di BulletDefault. |
| BulletTick | `5` | Il proiettile del primo livello è un personaggio di Wingding tick. I livelli rimanenti sono gli stessi di BulletDefault. |
| NumberDefault | `6` | Elenco numerato predefinito con 9 livelli. Numerazione araba (1., 2., 3., ...) per il primo livello, numerazione con lettere minuscole (a., b., c., ...) per il secondo livello, numerazione romana minuscola (i ., ii., iii., ...) per il terzo livello. Quindi la formattazione si ripete per i livelli rimanenti. |
| NumberArabicDot | `6` | Uguale a NumeroPredefinito. |
| NumberArabicParenthesis | `7` | Il numero del primo livello è "1)". I livelli rimanenti sono gli stessi di NumberDefault. |
| NumberUppercaseRomanDot | `8` | Il numero del primo livello è "I.". I livelli rimanenti sono gli stessi di NumberDefault. |
| NumberUppercaseLetterDot | `9` | Il numero del primo livello è "A.". I livelli rimanenti sono gli stessi di NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Il numero del primo livello è "a)". I livelli rimanenti sono gli stessi di NumberDefault. |
| NumberLowercaseLetterDot | `11` | Il numero del primo livello è "a.". I livelli rimanenti sono gli stessi di NumberDefault. |
| NumberLowercaseRomanDot | `12` | Il numero del primo livello è "i.". I livelli rimanenti sono gli stessi di NumberDefault. |
| OutlineNumbers | `13` | Un elenco schematico con i livelli numerati "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Un elenco schema con livelli è numerato "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Uno schema elenca con vari punti elenco per diversi livelli. |
| OutlineHeadingsArticleSection | `16` | Un elenco di struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsLegal | `17` | Un elenco di struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsNumbers | `18` | Un elenco di struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsChapter | `19` | Un elenco di struttura con livelli collegati agli stili di intestazione. |

### Osservazioni

Un valore del modello di elenco viene utilizzato come parametro in [`Add`](../listcollection/add/) metodo.

I modelli di elenco Aspose.Words corrispondono ai 21 modelli di elenco disponibili nella finestra di dialogo Punti elenco e numerazione in Microsoft Word 2003.

### Esempi

Mostra come creare un documento che contenga tutti i modelli di elenco di intestazioni di struttura.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Mostra come riavviare la numerazione in un elenco copiando un elenco.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizza il suo primo livello di elenco.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applica il nostro elenco ad alcuni paragrafi.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Possiamo aggiungere una copia di un elenco esistente alla raccolta di elenchi del documento
// per creare un elenco simile senza apportare modifiche all'originale.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Applica il secondo elenco ai nuovi paragrafi.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Mostra come lavorare con i livelli di elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello dell'elenco
// per iniziare un sottoelenco autonomo all'elemento dell'elenco corrente.
// Il modello di elenco di Microsoft Word chiamato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
// I livelli di elenco più profondi utilizzano lettere e numeri romani minuscoli. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un trattino e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "■" e "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Possiamo disabilitare la formattazione degli elenchi per non formattare i paragrafi successivi come elenchi deselezionando il flag "Elenco".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
