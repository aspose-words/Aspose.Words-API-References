---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words per .NET
description: Crea SmartTag dinamici senza sforzo con il nostro costruttore. Arricchisci i tuoi progetti con funzionalità personalizzabili e un'integrazione perfetta per prestazioni ottimali.
type: docs
weight: 10
url: /it/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Inizializza una nuova istanza di[`SmartTag`](../) classe.

```csharp
public SmartTag(DocumentBase doc)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |

## Osservazioni

Quando si crea un nuovo nodo, è necessario specificare un documento a cui appartiene. Un nodo non può esistere senza un documento perché dipende dalle strutture che lo compongono, come elenchi e stili. Sebbene un nodo appartenga sempre a un documento, potrebbe o meno far parte dell'albero del documento.

Quando un nodo viene creato, appartiene a un documento, ma non fa ancora parte dell'albero del documento e[`ParentNode`](../../../aspose.words/node/parentnode/) è nullo. Per inserire un nodo nel documento, usa [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) O[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)Metodi sul nodo padre.

## Esempi

Mostra come creare tag intelligenti.

```csharp
public void Create()
{
    Document doc = new Document();

    // Un tag intelligente appare in un documento con Microsoft Word che riconosce una parte del suo testo come una qualche forma di dati,
    // come un nome, una data o un indirizzo e lo converte in un collegamento ipertestuale che presenta una sottolineatura tratteggiata viola.
    SmartTag smartTag = new SmartTag(doc);

    // I tag intelligenti sono nodi compositi che contengono il testo riconosciuto nella sua interezza.
    // Aggiungere manualmente i contenuti a questo smart tag.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word potrebbe riconoscere il contenuto sopra riportato come una data.
    // I tag intelligenti utilizzano la proprietà "Element" per riflettere il tipo di dati che contengono.
    smartTag.Element = "date";

    // Alcuni tipi di smart tag elaborano ulteriormente il loro contenuto trasformandolo in proprietà XML personalizzate.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Imposta l'URI dello smart tag sul valore predefinito.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Crea un altro tag intelligente per un ticker azionario.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Stampa tutti gli smart tag nel nostro documento utilizzando un visitatore del documento.
    doc.Accept(new SmartTagPrinter());

    // Le versioni precedenti di Microsoft Word supportano i tag intelligenti.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Utilizzare il metodo "RemoveSmartTags" per rimuovere tutti i tag intelligenti da un documento.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Stampa gli smart tag visitati e il loro contenuto.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando termina la visita a un nodo SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Guarda anche

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
