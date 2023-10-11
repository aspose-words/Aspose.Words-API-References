---
title: Enum ListTemplate
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Lists.ListTemplate enum. Specifica uno dei formati di elenco predefiniti disponibili in Microsoft Word.
type: docs
weight: 3530
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
| BulletDisk | `0` | Uguale aBulletDefault. |
| BulletCircle | `1` | Il punto elenco del primo livello è un cerchio. I restanti livelli sono gli stessi diBulletDefault. |
| BulletSquare | `2` | Il punto elenco del primo livello è un quadrato. I restanti livelli sono gli stessi diBulletDefault. |
| BulletDiamonds | `3` | Il proiettile del primo livello è un personaggio Wingding a 4 diamanti. I restanti livelli sono gli stessi diBulletDefault. |
| BulletArrowHead | `4` | Il proiettile del primo livello è un personaggio alato con la punta di una freccia. I restanti livelli sono gli stessi diBulletDefault. |
| BulletTick | `5` | Il proiettile del primo livello è un segno di spunta del personaggio Wingding. I restanti livelli sono gli stessi diBulletDefault. |
| NumberDefault | `6` | Elenco numerato predefinito con 9 livelli. Numerazione araba (1., 2., 3., ...) per il primo livello, numerazione minuscola (a., b., c., ...) per il secondo livello, numerazione minuscola romana (i ., ii., iii., ...) per il terzo livello. Quindi la formattazione si ripete per i livelli rimanenti. |
| NumberArabicDot | `6` | Uguale aNumberDefault. |
| NumberArabicParenthesis | `7` | Il numero del primo livello è "1)". I restanti livelli sono gli stessi diNumberDefault. |
| NumberUppercaseRomanDot | `8` | Il numero del primo livello è "I.". I restanti livelli sono gli stessi diNumberDefault. |
| NumberUppercaseLetterDot | `9` | Il numero del primo livello è "A.". I restanti livelli sono gli stessi diNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Il numero del primo livello è "a)". I restanti livelli sono gli stessi diNumberDefault. |
| NumberLowercaseLetterDot | `11` | Il numero del primo livello è "a.". I restanti livelli sono gli stessi diNumberDefault. |
| NumberLowercaseRomanDot | `12` | Il numero del primo livello è "i.". I restanti livelli sono gli stessi diNumberDefault. |
| OutlineNumbers | `13` | Un elenco schematico con i livelli numerati "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Un elenco schematico con livelli è numerato "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Uno schema elenca con vari punti elenco per diversi livelli. |
| OutlineHeadingsArticleSection | `16` | Un elenco struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsLegal | `17` | Un elenco struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsNumbers | `18` | Un elenco struttura con livelli collegati agli stili di intestazione. |
| OutlineHeadingsChapter | `19` | Un elenco struttura con livelli collegati agli stili di intestazione. |

### Osservazioni

Un valore del modello di elenco viene utilizzato come parametro in the [`Add`](../listcollection/add/) metodo.

I modelli di elenco Aspose.Words corrispondono ai 21 modelli di elenco disponibili nella finestra di dialogo Elenchi puntati e numerati in Microsoft Word 2003.

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

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Crea un elenco da un modello Microsoft Word e personalizza il primo livello di elenco.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applica la nostra lista ad alcuni paragrafi.
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

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ciascun elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello della lista
// per iniziare un sottoelenco autonomo dall'elemento dell'elenco corrente.
// Il modello di elenco di Microsoft Word denominato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
 // I livelli di elenco più profondi utilizzano lettere e numeri romani minuscoli.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "***" e "○".
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


