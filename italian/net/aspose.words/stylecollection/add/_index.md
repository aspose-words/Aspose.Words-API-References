---
title: StyleCollection.Add
second_title: Aspose.Words per .NET API Reference
description: StyleCollection metodo. Crea un nuovo stile definito dallutente e lo aggiunge alla raccolta.
type: docs
weight: 60
url: /it/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Crea un nuovo stile definito dall'utente e lo aggiunge alla raccolta.

```csharp
public Style Add(StyleType type, string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| type | StyleType | UN[`StyleType`](../../styletype/) valore che specifica il tipo di stile da creare. |
| name | String | Nome dello stile da creare con distinzione tra maiuscole e minuscole. |

### Osservazioni

È possibile creare uno stile di carattere, paragrafo o elenco.

Quando si crea uno stile elenco, lo stile viene creato con la formattazione predefinita dell'elenco numerato (1 \ a \ i).

Genera un'eccezione se esiste già uno stile con questo nome.

### Esempi

Mostra come aggiungere uno stile alla raccolta di stili di un documento.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.DefaultFont.Name = "Courier New";

// Se aggiungiamo uno stile di "StyleType.Paragraph", la raccolta applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

Mostra come creare uno stile elenco e utilizzarlo in un documento.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Possiamo contenere un intero oggetto List all'interno di uno stile.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Modifica l'aspetto di tutti i livelli di elenco nel nostro elenco.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Crea un altro elenco da un elenco all'interno di uno stile.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Aggiungi alcuni elementi dell'elenco che il nostro elenco formatterà.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crea e applica un altro elenco in base allo stile dell'elenco.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Guarda anche

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* spazio dei nomi [Aspose.Words](../../stylecollection/)
* assemblea [Aspose.Words](../../../)


