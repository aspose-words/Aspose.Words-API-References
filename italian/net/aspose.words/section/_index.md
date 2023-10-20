---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words per .NET
description: Aspose.Words.Section classe. Rappresenta una singola sezione in un documento in C#.
type: docs
weight: 5730
url: /it/net/aspose.words/section/
---
## Section class

Rappresenta una singola sezione in un documento.

Per saperne di più, visita il[Lavorare con le sezioni](https://docs.aspose.com/words/net/working-with-sections/) articolo di documentazione.

```csharp
public sealed class Section : CompositeNode
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Inizializza una nuova istanza della classe Sezione. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Restituisce il[`Body`](../body/) nodo figlio della sezione. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Fornisce l'accesso ai nodi intestazioni e piè di pagina della sezione. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | RestituisceSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Restituisce un oggetto che rappresenta l'impostazione della pagina e le proprietà della sezione. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli, gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi secondari per questo nodo. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Inserisce una copia del contenuto della sezione sorgente alla fine di questa sezione. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Cancella la sezione. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Cancella le intestazioni e i piè di pagina di questa sezione. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Crea un duplicato di questa sezione. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Elimina tutte le forme (oggetti di disegno) dalle intestazioni e dai piè di pagina di questa sezione. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Garantisce che la sezione abbia[`Body`](./body/) con uno[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi secondari per questo nodo. |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Inserisce una copia del contenuto della sezione sorgente all'inizio di questa sezione. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

`Section` può averne uno[`Body`](../body/) e massimo uno[`HeaderFooter`](../headerfooter/) di ciascuno[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) E[`HeaderFooter`](../headerfooter/) nodes può essere in qualsiasi ordine all'interno`Section`.

È necessario avere una sezione minima valida[`Body`](../body/) con uno[`Paragraph`](../paragraph/).

Ogni sezione ha il proprio set di proprietà che specificano la dimensione della pagina, l'orientamento, i margini, ecc.

Puoi creare una copia di una sezione utilizzando[`Clone`](../node/clone/). La copia può essere inserita nello stesso documento o in un documento diverso.

Per aggiungere, inserire o rimuovere un'intera sezione, comprese le proprietà di interruzione di sezione e di sezione , utilizzare i metodi di[`Sections`](../document/sections/) oggetto.

Per copiare e inserire solo il contenuto della sezione escludendo la sezione break e le proprietà della sezione utilizzare[`AppendContent`](./appendcontent/) E[`PrependContent`](./prependcontent/) metodi.

## Esempi

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

* class [CompositeNode](../compositenode/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
