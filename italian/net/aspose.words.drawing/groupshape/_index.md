---
title: GroupShape
second_title: Aspose.Words per .NET API Reference
description: Rappresenta un gruppo di forme in un documento.
type: docs
weight: 890
url: /it/net/aspose.words.drawing/groupshape/
---
## GroupShape class

Rappresenta un gruppo di forme in un documento.

```csharp
public class GroupShape : ShapeBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [GroupShape](groupshape)(DocumentBase) | Crea una nuova forma di gruppo. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap) { get; set; } | Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext) { get; set; } | Definisce un testo alternativo da visualizzare invece di un grafico. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked) { get; set; } | Specifica se l'ancora della forma è bloccata. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked) { get; set; } | Specifica se le proporzioni della forma sono bloccate. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext) { get; set; } | Specifica se la forma è al di sotto o al di sopra del testo. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom) { get; } | Ottiene la posizione del bordo inferiore del blocco contenitore della forma. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds) { get; set; } | Ottiene o imposta la posizione e la dimensione del blocco contenitore della forma. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints) { get; } | Ottiene la posizione e la dimensione del blocco contenitore della forma in punti, rispetto all'ancora della forma più in alto. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects) { get; } | Ottiene l'estensione finale di questo oggetto forma dopo l'applicazione degli effetti di disegno. Il valore viene misurato in punti. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage) { get; } | Restituisce true se il tipo di forma consente alla forma di avere un'immagine. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ottiene tutti i nodi figlio immediati di questo nodo. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin) { get; set; } | Le coordinate nell'angolo in alto a sinistra del blocco contenitore di questa forma. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize) { get; set; } | La larghezza e l'altezza dello spazio delle coordinate all'interno del blocco contenitore di questa forma. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo inferiore della forma. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo sinistro della forma. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo superiore della forma. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Fill](../../aspose.words.drawing/shapebase/fill) { get; } | Ottiene la formattazione di riempimento per la forma. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ottiene il primo figlio del nodo. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation) { get; set; } | Cambia l'orientamento di una forma. |
| [Font](../../aspose.words.drawing/shapebase/font) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Restituisce true se questo nodo ha nodi figlio. |
| [Height](../../aspose.words.drawing/shapebase/height) { get; set; } | Ottiene o imposta l'altezza del blocco contenitore della forma. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment) { get; set; } | Specifica come posizionare la forma orizzontalmente. |
| [HRef](../../aspose.words.drawing/shapebase/href) { get; set; } | Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Restituisce true poiché questo nodo può avere nodi figlio. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative) { get; set; } | Ottiene o imposta il flag che specifica se la forma è decorativa nel documento. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup) { get; } | Restituisce vero se questa è una forma di gruppo. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule) { get; } | Restituisce vero se questa forma è una regola orizzontale. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage) { get; } | Restituisce vero se questa forma è una forma immagine. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline) { get; } | Un modo rapido per determinare se questa forma è posizionata in linea con il testo. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell) { get; set; } | Ottiene o imposta un flag che indica se la forma viene visualizzata all'interno o all'esterno di una tabella. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline) { get; } | Indica che la forma è una SignatureLine. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel) { get; } | Restituisce true se questa forma non è figlia di una forma di gruppo. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart) { get; } | Restituisce true se questa forma è un oggetto WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ottiene l'ultimo figlio del nodo. |
| [Left](../../aspose.words.drawing/shapebase/left) { get; set; } | Ottiene o imposta la posizione del bordo sinistro del blocco contenitore della forma. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage) { get; } | Ottiene MarkupLanguage utilizzato per questo oggetto grafico. |
| [Name](../../aspose.words.drawing/shapebase/name) { get; set; } | Ottiene o imposta il nome della forma opzionale. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype) { get; } | RestituisceGroupShape . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph) { get; } | Restituisce il paragrafo principale immediato. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition) { get; set; } | Specifica rispetto a cosa è posizionata orizzontalmente la forma. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition) { get; set; } | Specifica il posizionamento verticale della forma. |
| [Right](../../aspose.words.drawing/shapebase/right) { get; } | Ottiene la posizione del bordo destro del blocco contenitore della forma. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation) { get; set; } | Definisce l'angolo (in gradi) di rotazione di una forma. Il valore positivo corrisponde all'angolo di rotazione in senso orario. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip) { get; set; } | Definisce il testo visualizzato quando il puntatore del mouse si sposta sulla forma. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat) { get; } | Ottiene la formattazione dell'ombra per la forma. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype) { get; } | Ottiene il tipo di forma. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints) { get; } | Ottiene la dimensione della forma in punti. |
| [Target](../../aspose.words.drawing/shapebase/target) { get; set; } | Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma. |
| [Title](../../aspose.words.drawing/shapebase/title) { get; set; } | Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente. |
| [Top](../../aspose.words.drawing/shapebase/top) { get; set; } | Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment) { get; set; } | Specifica come posizionare la forma verticalmente. |
| [Width](../../aspose.words.drawing/shapebase/width) { get; set; } | Ottiene o imposta la larghezza del blocco contenitore della forma. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside) { get; set; } | Specifica come il testo viene avvolto attorno alla forma. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype) { get; set; } | Definisce se la forma è in linea o mobile. Per le forme mobili definisce la modalità di ritorno a capo per il testo attorno alla forma. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder) { get; set; } | Determina l'ordine di visualizzazione delle forme sovrapposte. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.drawing/groupshape/accept)(DocumentVisitor) | Accetta un visitatore. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects)(RectangleF) | Aggiunge al rettangolo di origine i valori dell'estensione dell'effetto e restituisce il rettangolo finale. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Riservato per l'uso del sistema. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr)(int) | Riservato per l'uso del sistema. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr)(int) | Riservato per l'uso del sistema. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Restituisce un ennesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr)(int) | Riservato per l'uso del sistema. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer)() | Crea e restituisce un oggetto che può essere utilizzato per rendere questa forma in un'immagine. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Restituisce l'indice del nodo figlio specificato nell'array del nodo figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent)(PointF) | Converte un valore dallo spazio delle coordinate locali nello spazio delle coordinate della forma padre. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Rimuove il nodo figlio specificato. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr)(int) | Riservato per l'uso del sistema. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Seleziona il primo nodo che corrisponde all'espressione XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr)(int, object) | Riservato per l'uso del sistema. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

UN[`GroupShape`](../groupshape) è un nodo composito e può avere[`Shape`](../shape) e [`GroupShape`](../groupshape) nodi da bambini.

A testa[`GroupShape`](../groupshape) definisce un nuovo sistema di coordinate per le sue forme figlie. Il sistema di coordinate viene definito utilizzando il[`CoordSize`](../shapebase/coordsize) e [`CoordOrigin`](../shapebase/coordorigin) proprietà.

### Esempi

Mostra come creare un gruppo di forme e stamparne il contenuto utilizzando un visitatore del documento.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Se devi creare forme "non primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornersRounded, TopCornersRounded, DiagonaleCornersRounded
    // usa i metodi DocumentBuilder.InsertShape.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200, 
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100, 
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Stampa il contenuto di un gruppo di forme visitato sulla console.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* class [ShapeBase](../shapebase)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
