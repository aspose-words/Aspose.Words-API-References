---
title: Class OfficeMath
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Math.OfficeMath сорт. Представляет объект Office Math такой как функция уравнение матрица и т.п. Может содержать дочерние элементы elements  включая фрагменты математического текста закладки комментарии и т. д.OfficeMath экземпляры и некоторые другие узлы.
type: docs
weight: 3880
url: /ru/net/aspose.words.math/officemath/
---
## OfficeMath class

Представляет объект Office Math, такой как функция, уравнение, матрица и т.п. Может содержать дочерние элементы elements , включая фрагменты математического текста, закладки, комментарии и т. д.`OfficeMath` экземпляры и некоторые другие узлы.

```csharp
public class OfficeMath : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает идентификатор пользовательского узла. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Получает/задает тип формата отображения Office Math, который указывает, отображается ли уравнение вместе с текстом или отображается на отдельной строке. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding/) { get; set; } | Получает/задает кодировку, которая использовалась для кодирования XML-уравнения, если этот офисный математический объект считывается из XML-уравнения. Мы используем кодировку при сохранении документа для записи в той же кодировке, в которой он был прочитан. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого потомка узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Получает/устанавливает выравнивание Office Math. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Получает тип[`MathObjectType`](./mathobjecttype/) этого объекта Office Math. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | Возвращает **NodeType.OfficeMath** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Извлекает родителя[`Paragraph`](../../aspose.words/paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Зарезервировано для системного использования. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Создает и возвращает объект, который можно использовать для преобразования этого уравнения в изображение. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

В этой версии Aspose.Words`OfficeMath` узлы не предоставляют общедоступные методы и свойства для создания или изменения объекта OfficeMath. В этой версии вы не можете создать экземпляр Math узлов или изменить существующие, кроме их удаления.

`OfficeMath` может быть только ребенком[`Paragraph`](../../aspose.words/paragraph/).

### Примеры

Показывает, как настроить формат отображения математических данных в офисе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Узлы OfficeMath, являющиеся потомками других узлов OfficeMath, всегда являются встроенными.
// Узел, с которым мы работаем, является базовым узлом для изменения его местоположения и типа отображения.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Форматы OOXML и WML используют свойство "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Измените расположение и тип отображения узла OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)


