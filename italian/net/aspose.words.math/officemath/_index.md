---
title: Class OfficeMath
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Math.OfficeMath classe. Rappresenta un oggetto Office Math come una funzione unequazione una matrice o simili. Può contenere elementi secondari tra cui sequenze di testo matematico segnalibri commenti e altroOfficeMathistanze e alcuni altri nodi.
type: docs
weight: 4120
url: /it/net/aspose.words.math/officemath/
---
## OfficeMath class

Rappresenta un oggetto Office Math come una funzione, un'equazione, una matrice o simili. Può contenere elementi secondari tra cui sequenze di testo matematico, segnalibri, commenti e altro`OfficeMath`istanze e alcuni altri nodi.

Per saperne di più, visita il[Lavorare con OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) articolo di documentazione.

```csharp
public class OfficeMath : CompositeNode
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Ottiene/imposta il tipo di formato di visualizzazione Office Math che indica se un'equazione viene visualizzata in linea con il testo o su una propria riga. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Ottiene/imposta la giustificazione matematica di Office. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Ottiene il tipo[`MathObjectType`](./mathobjecttype/) di questo oggetto Office Math. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | RestituisceOfficeMath . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../../aspose.words/range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Crea e restituisce un oggetto che può essere utilizzato per eseguire il rendering di questa equazione in un'immagine. |
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
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

In questa versione di Aspose.Words,`OfficeMath` i nodi non forniscono metodi pubblici e proprietà per creare o modificare a`OfficeMath` oggetto. In questa versione non puoi istanziare Math nodi o modificare esistenti tranne eliminarli.

`OfficeMath` può essere solo un figlio di[`Paragraph`](../../aspose.words/paragraph/).

### Esempi

Mostra come impostare la formattazione della visualizzazione della matematica di Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre in linea.
// Il nodo con cui stiamo lavorando è il nodo base per modificarne la posizione e il tipo di visualizzazione.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Modifica la posizione e il tipo di visualizzazione del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Guarda anche

* class [CompositeNode](../../aspose.words/compositenode/)
* spazio dei nomi [Aspose.Words.Math](../../aspose.words.math/)
* assemblea [Aspose.Words](../../)


