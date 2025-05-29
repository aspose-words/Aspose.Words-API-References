---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Shape per creare senza sforzo oggetti di disegno versatili come forme, caselle di testo e immagini nei tuoi progetti.
type: docs
weight: 1640
url: /it/net/aspose.words.drawing/shape/
---
## Shape class

Rappresenta un oggetto nel livello di disegno, ad esempio una forma automatica, una casella di testo, un oggetto libero, un oggetto OLE, un controllo ActiveX o un'immagine.

Per saperne di più, visita il[Lavorare con le forme](https://docs.aspose.com/words/net/working-with-shapes/) articolo di documentazione.

```csharp
public sealed class Shape : ShapeBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Crea un nuovo oggetto forma. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Adjustments](../../aspose.words.drawing/shape/adjustments/) { get; } | Fornisce l'accesso ai valori grezzi di regolazione di una forma. Per una forma che non contiene valori grezzi di regolazione, restituisce una raccolta vuota. |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Definisce il testo alternativo da visualizzare al posto di un'immagine. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Specifica se l'ancoraggio della forma è bloccato. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Specifica se le proporzioni della forma sono bloccate. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Specifica se la forma si trova sotto o sopra il testo. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Ottiene la posizione del bordo inferiore del blocco contenitore della forma. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Ottiene o imposta la posizione e la dimensione del blocco contenitore della forma. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Ottiene la posizione e la dimensione del blocco contenitore della forma in punti, rispetto all'ancoraggio della forma più in alto. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Ottiene l'estensione finale di questo oggetto forma dopo l'applicazione degli effetti di disegno. Il valore è misurato in punti. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Restituisce`VERO` se il tipo di forma consente alla forma di avere un'immagine. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Fornisce l'accesso alle proprietà del grafico se questa forma ha un[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Le coordinate nell'angolo in alto a sinistra del blocco contenitore di questa forma. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Larghezza e altezza dello spazio delle coordinate all'interno del blocco contenitore di questa forma. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo inferiore della forma. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo sinistro della forma. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo superiore della forma. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Restituisce`VERO` se è abilitato un effetto di estrusione. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Ottiene la formattazione di riempimento per la forma. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Definisce il colore del pennello che riempie il tracciato chiuso della forma. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Determina se il percorso chiuso della forma verrà riempito. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Ottiene il primo paragrafo nella forma. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Cambia l'orientamento di una forma. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Ottiene la formattazione bagliore per la forma. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Restituisce`VERO` se questo`Shape` ha un[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Restituisce`VERO` se la forma ha byte di immagine o collega un'immagine. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Restituisce`VERO` se questo`Shape` ha un oggetto SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Ottiene o imposta l'altezza del blocco contenitore della forma. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Ottiene o imposta il valore che rappresenta la percentuale dell'altezza relativa della forma. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Ottiene o imposta un valore booleano che indica se la forma è visibile. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Specifica come la forma è posizionata orizzontalmente. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Fornisce l'accesso alle proprietà della forma della regola orizzontale. Per una forma che non è una regola orizzontale, restituisce`null` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Fornisce l'accesso all'immagine della forma. Restituisce`null` se la forma non può avere un'immagine. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Ottiene o imposta il flag che specifica se la forma è decorativa nel documento. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Restituisce`VERO` se questa è una forma di gruppo. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Restituisce`VERO` se questa forma è una regola orizzontale. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Restituisce`VERO` se questa forma è una forma immagine. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Un modo rapido per determinare se questa forma è posizionata in linea con il testo. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Ottiene o imposta un flag che indica se la forma viene visualizzata all'interno di una tabella o all'esterno di essa. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indica che la forma è una[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Restituisce`VERO` se questa forma non è figlia di una forma di gruppo. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Restituisce`VERO` se questa forma è un oggetto WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo nella forma. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Ottiene o imposta la posizione del bordo sinistro del blocco contenitore della forma. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Ottiene o imposta il valore che rappresenta la posizione relativa a sinistra della forma in percentuale. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Ottiene il MarkupLanguage utilizzato per questo oggetto grafico. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Ottiene o imposta il nome facoltativo della forma. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | RestituisceShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Fornisce l'accesso ai dati OLE di una forma. Per una forma che non è un oggetto OLE o un controllo ActiveX, restituisce`null` . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Restituisce il paragrafo padre immediato. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Ottiene la formattazione della riflessione per la forma. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Specifica in relazione a cosa è posizionata orizzontalmente la forma. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Ottiene o imposta il valore della dimensione relativa della forma in direzione orizzontale. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Specifica in relazione a cosa è posizionata verticalmente la forma. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Ottiene o imposta il valore della dimensione relativa della forma in direzione verticale. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Ottiene la posizione del bordo destro del blocco contenitore della forma. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Definisce l'angolo (in gradi) di rotazione di una forma. Il valore positivo corrisponde all'angolo di rotazione in senso orario. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Definisce il testo visualizzato quando il puntatore del mouse si sposta sulla forma. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Restituisce`VERO` se è abilitato un effetto ombra. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Ottiene la formattazione dell'ombra per la forma. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Ottiene il tipo di forma. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Ottiene[`SignatureLine`](../signatureline/) oggetto se la forma è una riga della firma. Restituisce`null` altrimenti. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Ottiene la dimensione della forma in punti. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Ottiene la formattazione dei bordi sfumati per la forma. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | RestituisceTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Definisce un tratto per una forma. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Definisce il colore di un tratto. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Definisce se il percorso verrà tracciato. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Definisce lo spessore del pennello che traccia il percorso di una forma in punti. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Definisce gli attributi che specificano come viene visualizzato il testo in una forma. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Definisce il testo del percorso di testo (di un oggetto WordArt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Ottiene o imposta il valore che rappresenta la posizione superiore relativa della forma in percentuale. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Specifica come la forma è posizionata verticalmente. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Ottiene o imposta la larghezza del blocco contenitore della forma. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Ottiene o imposta il valore che rappresenta la percentuale della larghezza relativa della forma. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Specifica come il testo viene disposto attorno alla forma. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Definisce se la forma è in linea o mobile. Per le forme mobili, definisce la modalità di avvolgimento del testo attorno alla forma. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Determina l'ordine di visualizzazione delle forme sovrapposte. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato la fine della forma. |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio della forma. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Aggiunge al rettangolo sorgente i valori dell'estensione dell'effetto e restituisce il rettangolo finale. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Crea e restituisce un oggetto che può essere utilizzato per trasformare questa forma in un'immagine. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Converte un valore dallo spazio delle coordinate locali nello spazio delle coordinate della forma padre. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Aggiorna il disegno pre-renderizzato SmartArt utilizzando il motore di rendering a freddo SmartArt di Aspose.Words. |

## Osservazioni

Utilizzando il`Shape` classe puoi creare o modificare forme in un documento Microsoft Word.

Una proprietà importante di una forma è la sua[`ShapeType`](../shapebase/shapetype/)Forme di tipi diversi possono avere funzionalità diverse in un documento Word. Ad esempio, solo le forme immagine e OLE possono contenere immagini al loro interno. La maggior parte delle forme può contenere testo, ma non tutte.

Le forme che possono contenere testo possono contenere[`Paragraph`](../../aspose.words/paragraph/) e [`Table`](../../aspose.words.tables/table/) nodi come figli.

## Esempi

Mostra come inserire un'immagine mobile al centro di una pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'immagine mobile che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file singoli.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma con un'immagine come file nel file system locale.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // I dati immagine delle forme possono contenere immagini di molti possibili formati.
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Mostra come eliminare tutte le forme da un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci due forme insieme a una forma di gruppo con un'altra forma al suo interno.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// Rimuove tutti i nodi Forma dal documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Tutte le forme sono sparite, ma la forma del gruppo è ancora presente nel documento.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Rimuovi tutte le forme di gruppo separatamente.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* class [ShapeBase](../shapebase/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
