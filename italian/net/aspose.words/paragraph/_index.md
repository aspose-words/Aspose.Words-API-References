---
title: Paragraph
second_title: Aspose.Words per .NET API Reference
description: Rappresenta un paragrafo di testo.
type: docs
weight: 4150
url: /it/net/aspose.words/paragraph/
---
## Paragraph class

Rappresenta un paragrafo di testo.

```csharp
public class Paragraph : CompositeNode
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Paragraph](paragraph)(DocumentBase) | Inizializza una nuova istanza di **Paragrafo** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator) { get; } | Vero se questa interruzione di paragrafo è un separatore di stile. Un separatore di stile consente a un paragrafo di essere composto da parti con stili di paragrafo diversi. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ottiene tutti i nodi figlio immediati di questo nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ottiene il primo figlio del nodo. |
| [FrameFormat](../../aspose.words/paragraph/frameformat) { get; } | Fornisce l'accesso alle proprietà di formattazione del paragrafo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Restituisce true se questo nodo ha nodi figlio. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Restituisce true poiché questo nodo può avere nodi figlio. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell) { get; } | Vero se questo paragrafo è l'ultimo paragrafo in a[`Cell`](../../aspose.words.tables/cell) ; falso altrimenti. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument) { get; } | Vero se questo paragrafo è l'ultimo paragrafo nell'ultima sezione del documento. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter) { get; } | Vero se questo paragrafo è l'ultimo paragrafo del **HeaderFooter** (testo principale racconto) di a **Sezione** ; falso altrimenti. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection) { get; } | Vero se questo paragrafo è l'ultimo paragrafo del **Corpo** (testo principale racconto) di a **Sezione** ; falso altrimenti. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInCell](../../aspose.words/paragraph/isincell) { get; } | Vero se questo paragrafo è un figlio immediato di[`Cell`](../../aspose.words.tables/cell) ; falso altrimenti. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsListItem](../../aspose.words/paragraph/islistitem) { get; } | Vero quando il paragrafo è un elemento in un elenco puntato o numerato nella revisione originale. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ottiene l'ultimo figlio del nodo. |
| [ListFormat](../../aspose.words/paragraph/listformat) { get; } | Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo. |
| [ListLabel](../../aspose.words/paragraph/listlabel) { get; } | Ottiene a[`ListLabel`](./listlabel) oggetto che fornisce l'accesso al valore di numerazione dell'elenco e alla formattazione per questo paragrafo. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/paragraph/nodetype) { get; } | Restituisce **NodeType.Paragraph** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont) { get; } | Fornisce l'accesso alla formattazione del carattere del carattere di interruzione di paragrafo. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat) { get; } | Fornisce l'accesso alle proprietà di formattazione del paragrafo. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentSection](../../aspose.words/paragraph/parentsection) { get; } | Recupera il genitore[`Section`](../section) del paragrafo. |
| [ParentStory](../../aspose.words/paragraph/parentstory) { get; } | Recupera la storia a livello di sezione padre che può essere[`Body`](../body) o[`HeaderFooter`](../headerfooter) . |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [Runs](../../aspose.words/paragraph/runs) { get; } | Fornisce l'accesso alla raccolta digitata di parti di testo all'interno del paragrafo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept)(DocumentVisitor) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_1)(string) | Aggiunge un campo a questo paragrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield)(FieldType, bool) | Aggiunge un campo a questo paragrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_2)(string, string) | Aggiunge un campo a questo paragrafo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Riservato per l'uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Restituisce un ennesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops)() | Restituisce l'array di tutte le tabulazioni applicate a questo paragrafo, incluse quelle applicate indirettamente da stili o elenchi. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/paragraph/gettext)() | Ottiene il testo di questo paragrafo incluso il carattere di fine paragrafo. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Restituisce l'indice del nodo figlio specificato nell'array del nodo figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_1)(string, Node, bool) | Inserisce un campo in questo paragrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield)(FieldType, bool, Node, bool) | Inserisce un campo in questo paragrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_2)(string, string, Node, bool) | Inserisce un campo in questo paragrafo. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting)() | Join viene eseguito con la stessa formattazione nel paragrafo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Seleziona il primo nodo che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

[`Paragraph`](../paragraph) è un nodo a livello di blocco e può essere figlio di classi derivate da [`Story`](../story) o[`InlineStory`](../inlinestory).

[`Paragraph`](../paragraph) può contenere un numero qualsiasi di nodi e segnalibri a livello di linea.

L'elenco completo dei nodi figlio che possono verificarsi all'interno di un paragrafo è composto da [`BookmarkStart`](../bookmarkstart) ,[`BookmarkEnd`](../bookmarkend) , [`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) , [`FieldEnd`](../../aspose.words.fields/fieldend) ,[`FormField`](../../aspose.words.fields/formfield) , [`Comment`](../comment) ,[`Footnote`](../../aspose.words.notes/footnote) , [`Run`](../run) ,[`SpecialChar`](../specialchar) , [`Shape`](../../aspose.words.drawing/shape) ,[`GroupShape`](../../aspose.words.drawing/groupshape) , [`SmartTag`](../../aspose.words.markup/smarttag).

Un paragrafo valido in Microsoft Word termina sempre con un carattere di interruzione di paragrafo e un paragrafo valido minimo è costituito solo da un'interruzione di paragrafo. Il **Paragrafo** La classe aggiunge automaticamente il carattere di interruzione di paragrafo appropriato alla fine e questo carattere non fa parte dei nodi figlio della **Paragrafo** , quindi a **Paragrafo** può essere vuoto.

Non includere la fine del paragrafo[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak) o fine della cella[`ControlChar.Cell`](../controlchar/cell) caratteri all'interno del testo di il paragrafo in quanto potrebbe rendere il paragrafo non valido quando il documento viene aperto in Microsoft Word.

### Esempi

Mostra come costruire manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e finisci con un nodo documento senza figli.
doc.RemoveAllChildren();

// Questo documento ora non ha nodi figlio compositi a cui possiamo aggiungere contenuto.
// Se desideriamo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Innanzitutto, crea una nuova sezione, quindi aggiungila come figlio al nodo del documento radice.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per fare il documento. Crea una corsa,
// imposta l'aspetto e il contenuto, quindi aggiungilo come figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* class [CompositeNode](../compositenode)
* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
