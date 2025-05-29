---
title: OfficeMath Class
linktitle: OfficeMath
articleTitle: OfficeMath
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Math.OfficeMath, предназначенный для простого создания и управления объектами Office Math, такими как уравнения и матрицы.
type: docs
weight: 4810
url: /ru/net/aspose.words.math/officemath/
---
## OfficeMath class

Представляет объект Office Math, такой как функция, уравнение, матрица и т. п. Может содержать дочерние элементы , включая фрагменты математического текста, закладки, комментарии и т. д.`OfficeMath`экземпляры и некоторые другие узлы.

Чтобы узнать больше, посетите[Работа с OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) документальная статья.

```csharp
public class OfficeMath : CompositeNode
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DisplayType](../../aspose.words.math/officemath/displaytype/) { get; set; } | Возвращает/устанавливает тип формата отображения Office Math, который определяет, отображается ли уравнение в строке с текстом или отображается в отдельной строке. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [Justification](../../aspose.words.math/officemath/justification/) { get; set; } | Возвращает/устанавливает выравнивание Office Math. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype/) { get; } | Получает тип[`MathObjectType`](./mathobjecttype/)этого объекта Office Math. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.math/officemath/nodetype/) { get; } | ВозвратOfficeMath . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph/) { get; } | Возвращает родителя[`Paragraph`](../../aspose.words/paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.math/officemath/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца офиса math. |
| override [AcceptStart](../../aspose.words.math/officemath/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала офиса math. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer/)() | Создает и возвращает объект, который можно использовать для преобразования этого уравнения в изображение. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
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

В этой версии Aspose.Words,`OfficeMath` узлы не предоставляют публичные методы и свойства для создания или изменения`OfficeMath` объект. В этой версии вы не можете инстанцировать Math узлы или изменять существующие, за исключением их удаления.

`OfficeMath` может быть только ребенком[`Paragraph`](../../aspose.words/paragraph/).

## Примеры

Показывает, как настроить форматирование отображения офисных математических данных.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Узлы OfficeMath, являющиеся дочерними узлами других узлов OfficeMath, всегда являются встроенными.
// Узел, с которым мы работаем, является базовым узлом для изменения его местоположения и типа отображения.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Измените местоположение и тип отображения узла OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)
