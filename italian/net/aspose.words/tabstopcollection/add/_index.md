---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: TabStopCollection Add metodo. Aggiunge o sostituisce un punto di tabulazione nella raccolta in C#.
type: docs
weight: 30
url: /it/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Aggiunge o sostituisce un punto di tabulazione nella raccolta.

```csharp
public void Add(TabStop tabStop)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tabStop | TabStop | Un oggetto tabulazione da aggiungere. |

## Osservazioni

Se nella posizione specificata esiste già un punto di tabulazione, verrà sostituito.

## Esempi

Mostra come aggiungere tabulazioni personalizzate a un documento.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Di seguito sono riportati due modi per aggiungere punti di tabulazione alla raccolta di punti di tabulazione di un paragrafo tramite la proprietà "ParagraphFormat".
// 1 - Crea un oggetto "TabStop", quindi aggiungilo alla raccolta:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Passa i valori per le proprietà di una nuova tabulazione al metodo "Aggiungi":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Aggiunge tabulazioni a 5 cm a tutti i paragrafi.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Ogni carattere "tab" porta il cursore del builder nella posizione del punto di tabulazione successivo.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Guarda anche

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Aggiunge o sostituisce un punto di tabulazione nella raccolta.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| position | Double | Una posizione (in punti) in cui aggiungere la tabulazione. |
| alignment | TabAlignment | UN[`TabAlignment`](../../tabalignment/) valore that specifica l'allineamento del testo alla tabulazione. |
| leader | TabLeader | UN[`TabLeader`](../../tableader/) valore that specifica il tipo di linea guida visualizzata sotto il carattere di tabulazione. |

## Osservazioni

Se nella posizione specificata esiste già un punto di tabulazione, verrà sostituito.

## Esempi

Mostra come aggiungere tabulazioni personalizzate a un documento.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Di seguito sono riportati due modi per aggiungere punti di tabulazione alla raccolta di punti di tabulazione di un paragrafo tramite la proprietà "ParagraphFormat".
// 1 - Crea un oggetto "TabStop", quindi aggiungilo alla raccolta:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Passa i valori per le proprietà di una nuova tabulazione al metodo "Aggiungi":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Aggiunge tabulazioni a 5 cm a tutti i paragrafi.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Ogni carattere "tab" porta il cursore del builder nella posizione del punto di tabulazione successivo.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Guarda anche

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
