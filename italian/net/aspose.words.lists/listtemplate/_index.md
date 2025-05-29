---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Lists.ListTemplate, che include formati di elenco predefiniti di Microsoft Word per migliorare senza sforzo la presentazione del tuo documento.
type: docs
weight: 3980
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
| BulletDefault | `0` | Elenco puntato predefinito con 9 livelli. Il punto del primo livello è un disco, il punto del secondo livello è un cerchio, il punto del terzo livello è un quadrato. La formattazione si ripete per i livelli rimanenti. |
| BulletDisk | `0` | Lo stesso diBulletDefault. |
| BulletCircle | `1` | Il punto del primo livello è un cerchio. I livelli rimanenti sono gli stessi diBulletDefault. |
| BulletSquare | `2` | Il punto del primo livello è un quadrato. I livelli rimanenti sono gli stessi diBulletDefault. |
| BulletDiamonds | `3` | Il proiettile del primo livello è un personaggio Wingding a 4 diamanti. I livelli rimanenti sono gli stessi diBulletDefault. |
| BulletArrowHead | `4` | Il proiettile del primo livello è una punta di freccia raffigurante un personaggio Wingding. I livelli rimanenti sono gli stessi diBulletDefault. |
| BulletTick | `5` | Il proiettile del primo livello è un personaggio Wingding a forma di tick. I livelli rimanenti sono gli stessi diBulletDefault. |
| NumberDefault | `6` | Elenco numerato predefinito con 9 livelli. Numerazione araba (1., 2., 3., ...) per il primo livello, numerazione in lettere minuscole (a., b., c., ...) per il secondo livello, numerazione romana minuscola (i., ii., iii., ...) per il terzo livello. La formattazione si ripete quindi per i livelli rimanenti. |
| NumberArabicDot | `6` | Lo stesso diNumberDefault. |
| NumberArabicParenthesis | `7` | Il numero del primo livello è "1)". I livelli rimanenti sono gli stessi diNumberDefault. |
| NumberUppercaseRomanDot | `8` | Il numero del primo livello è "I". I livelli rimanenti sono gli stessi diNumberDefault. |
| NumberUppercaseLetterDot | `9` | Il numero del primo livello è "A". I livelli rimanenti sono gli stessi diNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Il numero del primo livello è "a)". I livelli rimanenti sono gli stessi diNumberDefault. |
| NumberLowercaseLetterDot | `11` | Il numero del primo livello è "a". I livelli rimanenti sono gli stessi diNumberDefault. |
| NumberLowercaseRomanDot | `12` | Il numero del primo livello è "i". I livelli rimanenti sono gli stessi diNumberDefault. |
| OutlineNumbers | `13` | Un elenco schematico con livelli numerati "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Un elenco schematico con livelli numerati "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Uno schema con vari punti elenco per diversi livelli. |
| OutlineHeadingsArticleSection | `16` | Un elenco strutturato con livelli collegati agli stili di intestazione. |
| OutlineHeadingsLegal | `17` | Un elenco strutturato con livelli collegati agli stili di intestazione. |
| OutlineHeadingsNumbers | `18` | Un elenco strutturato con livelli collegati agli stili di intestazione. |
| OutlineHeadingsChapter | `19` | Un elenco strutturato con livelli collegati agli stili di intestazione. |

## Osservazioni

Un valore di modello di elenco viene utilizzato come parametro in [`Add`](../listcollection/add/) metodo.

I modelli di elenco Aspose.Words corrispondono ai 21 modelli di elenco disponibili nella finestra di dialogo Elenchi puntati e numerati in Microsoft Word 2003.

## Esempi

Mostra come creare un documento contenente tutti i modelli di elenco delle intestazioni.

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

Mostra come riavviare la numerazione in un elenco copiando l'elenco stesso.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizzane il primo livello.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applichiamo il nostro elenco ad alcuni paragrafi.
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

Mostra come lavorare con i livelli degli elenchi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ogni elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello dell'elenco
// per iniziare un sottoelenco autonomo a partire dall'elemento corrente dell'elenco.
// Il modello di elenco di Microsoft Word denominato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
 // I livelli più profondi dell'elenco utilizzano lettere e numeri romani minuscoli.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "■" e "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Possiamo disabilitare la formattazione dell'elenco per non formattare i paragrafi successivi come elenchi deselezionando il flag "Elenco".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)
