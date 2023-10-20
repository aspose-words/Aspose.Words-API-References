---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words per .NET
description: Aspose.Words.Paragraph classe. Rappresenta un paragrafo di testo in C#.
type: docs
weight: 4390
url: /it/net/aspose.words/paragraph/
---
## Paragraph class

Rappresenta un paragrafo di testo.

Per saperne di più, visita il[Lavorare con i paragrafi](https://docs.aspose.com/words/net/working-with-paragraphs/) articolo di documentazione.

```csharp
public class Paragraph : CompositeNode
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Inizializza una nuova istanza di`Paragraph` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | Vero se questa interruzione di paragrafo è un separatore di stile. Un separatore di stile consente a un paragrafo di essere costituito da parti con stili di paragrafo diversi. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione del frame. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Vero se questo paragrafo è l'ultimo paragrafo in a[`Cell`](../../aspose.words.tables/cell/) ; falso altrimenti. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Vero se questo paragrafo è l'ultimo paragrafo dell'ultima sezione del documento. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Vero se questo paragrafo è l'ultimo paragrafo del[`HeaderFooter`](../headerfooter/) (storia del testo principale) di a[`Section`](../section/) ; falso altrimenti. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Vero se questo paragrafo è l'ultimo paragrafo del[`Body`](../body/) (storia del testo principale) di a[`Section`](../section/) ; falso altrimenti. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Vero se questo paragrafo è un figlio immediato di[`Cell`](../../aspose.words.tables/cell/) ; falso altrimenti. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Vero quando il paragrafo è un elemento in un elenco puntato o numerato nella revisione originale. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Ottiene a[`ListLabel`](./listlabel/)oggetto che fornisce l'accesso al valore di numerazione dell'elenco e alla formattazione per questo paragrafo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | RestituisceParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Fornisce l'accesso alla formattazione del carattere del carattere di interruzione di paragrafo. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione del paragrafo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Recupera il genitore[`Section`](../section/) del paragrafo. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Recupera la storia a livello di sezione principale che può essere[`Body`](../body/) O[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Fornisce l'accesso alla raccolta digitata di parti di testo all'interno del paragrafo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi secondari per questo nodo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Aggiunge un campo a questo paragrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Aggiunge un campo a questo paragrafo. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Aggiunge un campo a questo paragrafo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Restituisce l'array di tutti i punti di tabulazione applicati a questo paragrafo, inclusi quelli applicati indirettamente da stili o elenchi. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Ottiene il testo di questo paragrafo incluso il carattere di fine paragrafo. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Inserisce un campo in questo paragrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Inserisce un campo in questo paragrafo. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Inserisce un campo in questo paragrafo. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | I join vengono eseguiti con la stessa formattazione nel paragrafo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi secondari per questo nodo. |
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

`Paragraph` è un nodo a livello di blocco e può essere figlio di classi derivate da [`Story`](../story/) O[`InlineStory`](../inlinestory/).

`Paragraph` può contenere un numero qualsiasi di nodi e segnalibri a livello in linea.

L'elenco completo dei nodi figlio che possono verificarsi all'interno di un paragrafo è costituito da [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Un paragrafo valido in Microsoft Word termina sempre con un carattere di interruzione di paragrafo e un paragrafo valido minimo è costituito solo da un'interruzione di paragrafo. IL`Paragraph` La classe aggiunge automaticamente il carattere di interruzione di paragrafo appropriato alla fine e questo carattere non fa parte dei nodi figlio della classe`Paragraph` , quindi a`Paragraph` può essere vuoto.

Non includere la fine del paragrafo[`ParagraphBreak`](../controlchar/paragraphbreak/) o fine della cella[`Cell`](../controlchar/cell/) caratteri all'interno del testo di il paragrafo in quanto potrebbe rendere il paragrafo non valido quando il documento viene aperto in Microsoft Word.

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
