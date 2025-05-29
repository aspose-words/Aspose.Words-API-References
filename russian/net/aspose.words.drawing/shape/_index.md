---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Shape для легкого создания в ваших проектах универсальных объектов рисования, таких как автофигуры, текстовые поля и изображения.
type: docs
weight: 1640
url: /ru/net/aspose.words.drawing/shape/
---
## Shape class

Представляет объект на слое чертежа, например автофигуру, текстовое поле, произвольную форму, объект OLE, элемент управления ActiveX или изображение.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

```csharp
public sealed class Shape : ShapeBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Создает новый объект формы. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Adjustments](../../aspose.words.drawing/shape/adjustments/) { get; } | Предоставляет доступ к необработанным значениям корректировки фигуры. Для фигуры, которая не содержит необработанных значений корректировки, возвращается пустая коллекция. |
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
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Предоставляет доступ к свойствам диаграммы, если эта фигура имеет[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | Координаты в верхнем левом углу содержащего блока этой формы. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | Ширина и высота координатного пространства внутри содержащего блока этой формы. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и нижним краем фигуры. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Возвращает или задает расстояние (в пунктах) между текстом документа и верхним краем фигуры. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Возврат`истинный` если эффект выдавливания включен. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Получает форматирование заливки для фигуры. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Определяет цвет кисти, заполняющей замкнутый контур фигуры. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Определяет, будет ли заполнен замкнутый контур фигуры. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Получает первый абзац в форме. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Изменяет ориентацию фигуры. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Получает форматирование свечения для фигуры. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Возврат`истинный` если это`Shape` имеет[`Chart`](../../aspose.words.drawing.charts/chart/) . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Возврат`истинный` если форма имеет байты изображения или ссылается на изображение. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Возврат`истинный` если это`Shape` имеет объект SmartArt. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Возвращает или задает высоту содержащего блока фигуры. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Возвращает или задает значение, представляющее процент относительной высоты фигуры. |
| [Hidden](../../aspose.words.drawing/shapebase/hidden/) { get; set; } | Возвращает или задает логическое значение, указывающее, видна ли фигура. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Указывает, как фигура располагается по горизонтали. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Предоставляет доступ к свойствам формы горизонтальной линейки. Для формы, которая не является горизонтальной линейкой, возвращает`нулевой` . |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Получает или задает полный адрес гиперссылки для фигуры. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Предоставляет доступ к изображению фигуры. Возвращает`нулевой` если форма не может иметь изображение. |
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
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Получает последний абзац в форме. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Возвращает или задает положение левого края содержащего блока фигуры. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Возвращает или задает значение, представляющее относительное левое положение фигуры в процентах. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Получает MarkupLanguage, используемый для этого графического объекта. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Получает или задает необязательное имя фигуры. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | ВозвратShape . |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Предоставляет доступ к данным OLE фигуры. Для фигуры, которая не является объектом OLE или элементом управления ActiveX, возвращает`нулевой` . |
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
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Возврат`истинный` если включен эффект тени. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Получает форматирование тени для фигуры. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Получает тип фигуры. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Получает[`SignatureLine`](../signatureline/) объект, если фигура является линией подписи. Возвращает`нулевой` в противном случае. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Получает размер фигуры в точках. |
| [SoftEdge](../../aspose.words.drawing/shapebase/softedge/) { get; } | Получает мягкое форматирование краев для фигуры. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | ВозвратTextbox . |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Определяет обводку для фигуры. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Определяет цвет обводки. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Определяет, будет ли контур обведен. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Определяет толщину кисти, обводящей контур фигуры, в точках. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Получает или задает целевой фрейм для гиперссылки формы. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Определяет атрибуты, которые указывают, как текст отображается в форме. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Определяет текст текстового пути (объекта WordArt). |
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
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца фигуры. |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала фигуры. |
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
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Обновляет предварительно отрисованный рисунок SmartArt с помощью движка холодного рендеринга SmartArt от Aspose.Words. |

## Примечания

Используя`Shape` класс позволяет создавать или изменять фигуры в документе Microsoft Word.

Важным свойством фигуры является ее[`ShapeType`](../shapebase/shapetype/)Фигуры различных типов могут иметь разные возможности в документе Word. Например, только image и OLE shape могут иметь изображения внутри себя. Большинство фигур могут иметь текст, но не все.

Формы, которые могут иметь текст, могут содержать[`Paragraph`](../../aspose.words/paragraph/) и [`Table`](../../aspose.words.tables/table/) узлы как дочерние.

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

Показывает, как извлекать изображения из документа и сохранять их в локальной файловой системе в виде отдельных файлов.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Получить коллекцию фигур из документа,
// и сохранить данные изображения каждой фигуры с изображением в виде файла в локальной файловой системе.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Данные изображений фигур могут содержать изображения многих возможных форматов изображений.
        // Мы можем автоматически определить расширение файла для каждого изображения на основе его формата.
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

// Все фигуры исчезли, но групповая фигура все еще осталась в документе.
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
