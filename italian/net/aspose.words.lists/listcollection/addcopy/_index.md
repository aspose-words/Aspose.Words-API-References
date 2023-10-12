---
title: ListCollection.AddCopy
second_title: Aspose.Words per .NET API Reference
description: ListCollection metodo. Crea un nuovo elenco copiando lelenco specificato e aggiungendolo alla raccolta di elenchi nel documento.
type: docs
weight: 50
url: /it/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Crea un nuovo elenco copiando l'elenco specificato e aggiungendolo alla raccolta di elenchi nel documento.

```csharp
public List AddCopy(List srcList)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcList | List | L'elenco delle origini da cui copiare. |

### Valore di ritorno

L'elenco appena creato.

### Osservazioni

L'elenco delle origini può provenire da qualsiasi documento. Se l'elenco di origine appartiene a un documento diverso, viene creata una copia dell'elenco e aggiunta al documento corrente.

Se l'elenco di origine è un riferimento o una definizione di uno stile di elenco, l'elenco appena creato non è correlato allo stile di elenco originale.

### Esempi

Mostra come creare un documento con un campione di tutti gli elenchi di un altro documento.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
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

### Guarda anche

* class [List](../../list/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../listcollection/)
* assemblea [Aspose.Words](../../../)


