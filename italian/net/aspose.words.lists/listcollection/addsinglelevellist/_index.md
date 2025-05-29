---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words per .NET
description: Crea e aggiungi senza sforzo un elenco a livello singolo al tuo documento con il metodo AddSingleLevelList di ListCollection, migliorando l'organizzazione e la chiarezza.
type: docs
weight: 60
url: /it/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Crea un nuovo elenco a livello singolo basato sul modello predefinito e lo aggiunge alla raccolta di elenchi nel documento.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Esempi

Mostra come creare un nuovo elenco a livello singolo basato sul modello predefinito.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Crea l'elenco puntato dal modello BulletCircle.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Scrive l'elenco puntato nel documento risultante.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Crea l'elenco numerato dal modello NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Scrive l'elenco numerato nel documento risultante.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Guarda anche

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
