---
title: GroupShape
second_title: Справочник по API Aspose.Words для .NET
description: Представляет группу фигур в документе.
type: docs
weight: 890
url: /ru/net/aspose.words.drawing/groupshape/
---
## GroupShape class

Представляет группу фигур в документе.

```csharp
public class GroupShape : ShapeBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [GroupShape](groupshape/)(DocumentBase) | Создает новую форму группы. |

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
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Получает формат заливки для фигуры. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого потомка узла. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Переключает ориентацию фигуры. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Получает или задает высоту содержащего блока фигуры. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Определяет горизонтальное расположение фигуры. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Получает или задает полный адрес гиперссылки для фигуры. |
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
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Получает или задает положение левого края содержащего блока фигуры. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Получает язык разметки, используемый для этого графического объекта. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Получает или задает необязательное имя формы. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | ВозвращаетGroupShape . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Возвращает ближайший родительский абзац. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Определяет относительное положение фигуры по горизонтали. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Указывает, относительно чего фигура расположена вертикально. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Получает положение правого края содержащего блока фигуры. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Определяет текст, отображаемый при наведении указателя мыши на фигуру. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Получает форматирование тени для фигуры. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Получает тип фигуры. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Получает размер фигуры в точках. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Получает или задает целевой кадр для гиперссылки формы. |
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
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(DocumentVisitor) | Принимает посетителя. |
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

### Примечания

А[`GroupShape`](./groupshape/) является составным узлом и может иметь[`Shape`](../shape/) и [`GroupShape`](./groupshape/) узлы как дети.

Каждый[`GroupShape`](./groupshape/) определяет новую систему координат для своих дочерних фигур. Система координат определяется с помощью[`CoordSize`](../shapebase/coordsize/) и [`CoordOrigin`](../shapebase/coordorigin/) характеристики.

### Примеры

Показывает, как создать группу фигур и распечатать ее содержимое с помощью посетителя документа.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Если вам нужно создать "непримитивные" фигуры, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // используйте методы DocumentBuilder.InsertShape.
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
/// Выводит содержимое посещенной группы форм на консоль.
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

### Смотрите также

* class [ShapeBase](../shapebase/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
