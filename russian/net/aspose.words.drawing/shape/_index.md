---
title: Shape
second_title: Справочник по API Aspose.Words для .NET
description: Представляет объект в слое рисования например автофигуру текстовое поле произвольную форму объект OLE элемент управления ActiveX или изображение.
type: docs
weight: 1100
url: /ru/net/aspose.words.drawing/shape/
---
## Shape class

Представляет объект в слое рисования, например автофигуру, текстовое поле, произвольную форму, объект OLE, элемент управления ActiveX или изображение.

```csharp
public sealed class Shape : ShapeBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Shape](shape/)(DocumentBase, ShapeType) | Создает новый объект формы. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Получает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Определяет альтернативный текст, который будет отображаться вместо графики. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Указывает, заблокирована ли привязка фигуры. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Указывает, заблокировано ли соотношение сторон фигуры. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Указывает, находится ли фигура ниже или выше текста. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Получает положение нижнего края содержащего блока фигуры. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Получает или задает расположение и размер содержащего блока фигуры. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Получает расположение и размер содержащего блока фигуры в пунктах относительно привязки самой верхней фигуры. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Получает окончательный размер, который имеет этот объект формы после применения эффектов рисования. Значение измеряется в пунктах. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Возвращает true, если тип фигуры позволяет фигуре иметь изображение. |
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Предоставляет доступ к свойствам диаграммы, если эта фигура имеет Chart. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Координаты в верхнем левом углу содержащего блока этой формы. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Ширина и высота координатного пространства внутри содержащего блока этой фигуры. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает идентификатор пользовательского узла. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Возвращает true, если включен эффект выдавливания. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Получает формат заливки для фигуры. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Определяет цвет кисти, заполняющий замкнутый контур фигуры. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Определяет, будет ли заполнен замкнутый контур фигуры. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого потомка узла. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Получает первый абзац в форме. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Переключает ориентацию фигуры. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Возвращает true, если эта фигура имеет[`Chart`](./chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Возвращает true, если фигура содержит байты изображения или ссылается на изображение. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Возвращает true, если у этой формы есть объект SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Получает или задает высоту содержащего блока фигуры. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Определяет горизонтальное расположение фигуры. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Предоставляет доступ к свойствам фигуры горизонтальной линейки. Для фигуры, не являющейся горизонтальной линейкой, возвращает null. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Получает или задает полный адрес гиперссылки для фигуры. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Предоставляет доступ к изображению фигуры. Возвращает значение null, если фигура не может иметь изображение. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Получает или задает флаг, указывающий, является ли фигура декоративной в документе. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Возвращает true, если это форма группы. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Возвращает true, если эта фигура является горизонтальной линейкой. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Возвращает true, если эта форма является фигурой изображения. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Быстрый способ определить, расположена ли эта фигура на одной линии с текстом. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Возвращает **истинный** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Возвращает **истинный** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Указывает, что форма является SignatureLine. |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Возвращает true, если эта фигура не является дочерней фигурой группы. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Возвращает значение true, если эта фигура является объектом WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Получает последний абзац в форме. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Получает или задает положение левого края содержащего блока фигуры. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Получает язык разметки, используемый для этого графического объекта. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Получает или задает необязательное имя формы. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | ВозвращаетShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Предоставляет доступ к данным OLE формы. Для фигуры, которая не является объектом OLE или элементом управления ActiveX, возвращает null. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Возвращает ближайший родительский абзац. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Определяет относительное положение фигуры по горизонтали. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Указывает, относительно чего фигура расположена вертикально. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Получает положение правого края содержащего блока фигуры. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Возвращает true, если включен эффект тени. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Получает форматирование тени для фигуры. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Получает тип фигуры. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | получает[`SignatureLine`](./signatureline/) объект, если фигура является линией подписи. Возвращает **нулевой** иначе. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Получает размер фигуры в точках. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | ВозвращаетTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Определяет обводку фигуры. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Определяет цвет обводки. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Определяет, будет ли обведен контур. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Определяет толщину кисти, которая обводит контур фигуры в пунктах. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Получает или задает целевой кадр для гиперссылки формы. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Определяет атрибуты, определяющие способ отображения текста в фигуре. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Определяет текст текстового пути (объекта WordArt). |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Получает или задает заголовок (заголовок) текущего объекта формы. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Получает или задает положение верхнего края содержащего блока фигуры. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Определяет вертикальное расположение фигуры. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Получает или задает ширину содержащего блока фигуры. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Указывает, как текст оборачивает фигуру. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Определяет порядок отображения перекрывающихся фигур. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.drawing/shape/accept/)(DocumentVisitor) | Принимает посетителя. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(RectangleF) | Добавляет к исходному прямоугольнику значения экстента эффекта и возвращает окончательный прямоугольник. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Зарезервировано для системного использования. IXPathNavigable. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(int) | Зарезервировано для системного использования. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(int) | Зарезервировано для системного использования. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(int) | Зарезервировано для системного использования. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Создает и возвращает объект, который можно использовать для преобразования этой формы в изображение. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(PointF) | Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Удаляет указанный дочерний узел. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(int) | Зарезервировано для системного использования. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(int, object) | Зарезервировано для системного использования. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Обновляет предварительно обработанный рисунок SmartArt с помощью механизма холодного рендеринга Aspose.Words SmartArt. |

### Примечания

С использованием[`Shape`](./shape/) class вы можете создавать или изменять фигуры в документе Microsoft Word.

Важным свойством формы является ее[`ShapeType`](../shapebase/shapetype/). Формы типов different могут иметь разные возможности в документе Word. Например, только image и OLE shape могут содержать внутри себя изображения. Большинство фигур могут иметь текст, но не все.

Фигуры, которые могут иметь текст, могут содержать[`Paragraph`](../../aspose.words/paragraph/) и [`Table`](../../aspose.words.tables/table/) узлы как дети.

### Примеры

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте плавающее изображение, которое будет отображаться за перекрывающимся текстом, и выровняйте его по центру страницы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Показывает, как извлекать изображения из документа и сохранять их в локальной файловой системе в виде отдельных файлов.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Получить набор фигур из документа,
// и сохранить данные изображения каждой фигуры с изображением в виде файла в локальной файловой системе.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Данные изображения фигур могут содержать изображения многих возможных форматов изображений. 
        // Мы можем определить расширение файла для каждого изображения автоматически, исходя из его формата.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Показывает, как удалить все фигуры из документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте две фигуры вместе с групповой фигурой, внутри которой находится еще одна фигура.
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

// Удалить все узлы Shape из документа.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// Все фигуры исчезли, но фигура группы осталась в документе.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Удалить все групповые фигуры по отдельности.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Смотрите также

* class [ShapeBase](../shapebase/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
