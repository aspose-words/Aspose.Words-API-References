---
title: ShapeBase Class
linktitle: ShapeBase
articleTitle: ShapeBase
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Drawing.ShapeBase — основу для создания динамических рисунков, включая автофигуры, объекты OLE и элементы управления ActiveX.
type: docs
weight: 1650
url: /ru/net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Базовый класс для объектов в слое чертежа, таких как автофигуры, произвольные формы, объекты OLE, элементы управления ActiveX или изображения.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

```csharp
public abstract class ShapeBase : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Возвращает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Определяет альтернативный текст, отображаемый вместо графики. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Указывает, заблокирована ли привязка фигуры. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Указывает, заблокировано ли соотношение сторон фигуры. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Указывает, находится ли фигура под или над текстом. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Получает положение нижнего края содержащего блока фигуры. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Возвращает или задает местоположение и размер содержащего блока фигуры. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Получает местоположение и размер содержащего блока фигуры в пунктах относительно точки привязки самой верхней фигуры. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Получает окончательную протяженность объекта-фигуры после применения эффектов рисования. Значение измеряется в точках. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Возврат`истинный` если тип фигуры позволяет фигуре иметь изображение. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Координаты в верхнем левом углу содержащего блока этой формы. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Ширина и высота координатного пространства внутри содержащего блока этой формы. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Получает форматирование заливки для фигуры. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Изменяет ориентацию фигуры. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Получает форматирование свечения для фигуры. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Возвращает или задает высоту содержащего блока фигуры. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Возвращает или задает значение, представляющее процент относительной высоты фигуры. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Возвращает или задает логическое значение, указывающее, видна ли фигура. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Указывает, как фигура располагается по горизонтали. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Получает или задает полный адрес гиперссылки для фигуры. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Возвращает или задает флаг, указывающий, является ли фигура декоративной в документе. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Возврат`истинный` если это групповая форма. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Возврат`истинный` если эта фигура является горизонтальной линейкой. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Возврат`истинный` если эта форма является формой изображения. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | Быстрый способ определить, расположена ли эта фигура в одной строке с текстом. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Возвращает или задает флаг, указывающий, отображается ли фигура внутри таблицы или вне ее. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Указывает, что форма является[`SignatureLine`](../signatureline/) . |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Возврат`истинный` если эта фигура не является дочерней по отношению к группе фигур. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Возврат`истинный` если эта фигура является объектом WordArt. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Возвращает или задает положение левого края содержащего блока фигуры. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Возвращает или задает значение, представляющее относительное левое положение фигуры в процентах. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Получает MarkupLanguage, используемый для этого графического объекта. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Получает или задает необязательное имя фигуры. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Получает тип этого узла. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Возвращает непосредственный родительский абзац. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Получает форматирование отражения для фигуры. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Указывает, относительно чего фигура расположена горизонтально. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Возвращает или задает значение относительного размера фигуры в горизонтальном направлении. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Указывает, относительно чего фигура расположена по вертикали. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Возвращает или задает значение относительного размера фигуры в вертикальном направлении. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Получает положение правого края содержащего блока фигуры. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Определяет текст, отображаемый при перемещении указателя мыши по фигуре. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Получает форматирование тени для фигуры. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Получает тип фигуры. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Получает размер фигуры в точках. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Получает мягкое форматирование краев для фигуры. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Получает или задает целевой фрейм для гиперссылки формы. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Возвращает или задает заголовок (подпись) текущего объекта фигуры. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Возвращает или задает положение верхнего края содержащего блока фигуры. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Возвращает или задает значение, представляющее относительное верхнее положение фигуры в процентах. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Указывает, как фигура располагается по вертикали. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Возвращает или задает ширину содержащего блока фигуры. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Возвращает или задает значение, представляющее процент относительной ширины фигуры. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Указывает, как текст обтекает фигуру. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Определяет, является ли фигура встроенной или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Определяет порядок отображения перекрывающихся фигур. |

## Методы

| Имя | Описание |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | При реализации в производном классе вызывает метод VisitXXXEnd указанного посетителя документа. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | При реализации в производном классе вызывает метод VisitXXXStart указанного посетителя документа. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Добавляет к исходному прямоугольнику значения степени эффекта и возвращает конечный прямоугольник. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Создает и возвращает объект, который можно использовать для преобразования этой фигуры в изображение. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) что соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Это абстрактный класс. Два производных класса, которые вы можете инстанцировать , это[`Shape`](../shape/) и[`GroupShape`](../groupshape/).

Фигура — это узел в дереве документа.

Если форма является потомком[`Paragraph`](../../aspose.words/paragraph/) объект, то говорят, что фигура «верхнего уровня». Фигуры верхнего уровня измеряются и позиционируются в точках.

Форма также может быть потомком[`GroupShape`](../groupshape/) объект, когда несколько shape сгруппированы. Дочерние фигуры групповой фигуры располагаются в координатном пространстве, а units определяются[`CoordSize`](./coordsize/) и[`CoordOrigin`](./coordorigin/) свойства групповой формы parent .

Фигура может быть расположена в строке с текстом или плавающей. Метод позиционирования — controled с использованием[`WrapType`](./wraptype/) свойство.

Когда фигура плавающая, она позиционируется относительно чего-либо (например, текущего абзаца, поля или страницы). Относительное позиционирование фигуры указывается с помощью [`RelativeHorizontalPosition`](./relativehorizontalposition/) и[`RelativeVerticalPosition`](./relativeverticalposition/) характеристики.

Плавающая фигура может быть позиционирована явно с помощью[`Left`](./left/) и[`Top`](./top/) свойства или выровнены относительно какого-либо другого объекта с помощью[`HorizontalAlignment`](./horizontalalignment/) и[`VerticalAlignment`](./verticalalignment/) характеристики.

## Примеры

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

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
