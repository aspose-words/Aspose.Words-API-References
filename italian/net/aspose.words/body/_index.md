---
title: Class Body
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Body classe. Rappresenta un contenitore per il testo principale di una sezione.
type: docs
weight: 30
url: /it/net/aspose.words/body/
---
## Body class

Rappresenta un contenitore per il testo principale di una sezione.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class Body : Story
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Body](body/)(DocumentBase) | Inizializza una nuova istanza di`Body` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | RestituisceBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Ottiene la sezione principale di questa storia. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ottiene il tipo di questa storia. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ottiene una raccolta di tabelle che sono figli immediati della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(DocumentVisitor) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | Un metodo di scelta rapida che crea un file[`Paragraph`](../paragraph/) oggetto con testo facoltativo e lo aggiunge alla fine di questo oggetto. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Elimina tutte le forme dal testo di questa storia. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

`Body` può contenere[`Paragraph`](../paragraph/) E[`Tavolo`](../../aspose.words.tables/table/) nodi figli.

`Body` è un nodo a livello di sezione e può essere solo figlio di[`Section`](../section/) . Può essercene solo uno`Body` in un[`Section`](../section/).

Un minimo valido`Body` deve contenerne almeno uno[`Paragraph`](../paragraph/).

### Esempi

Mostra come costruire manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti questi nodi,
// e finiamo con un nodo documento senza figli.
doc.RemoveAllChildren();

// Questo documento ora non ha nodi secondari compositi a cui possiamo aggiungere contenuto.
// Se desideriamo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Innanzitutto, crea una nuova sezione, quindi aggiungila come figlia al nodo del documento root.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione necessita di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi lo aggiunge come figlio al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per realizzare il documento. Crea una corsa,
// ne imposta l'aspetto e il contenuto, quindi lo aggiunge come figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* class [Story](../story/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


