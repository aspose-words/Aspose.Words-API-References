---
title: SmartTag Class
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Markup.SmartTag, который расширяет возможности редактирования документов, определяя смарт-теги вокруг встроенных элементов, таких как изображения и поля.
type: docs
weight: 4740
url: /ru/net/aspose.words.markup/smarttag/
---
## SmartTag class

Этот элемент определяет наличие смарт-тега вокруг одной или нескольких встроенных структур (выступов, изображений, полей и т. д.) внутри абзаца.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class SmartTag : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SmartTag](smarttag/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Инициализирует новый экземпляр`SmartTag` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [Element](../../aspose.words.markup/smarttag/element/) { get; set; } | Указывает имя смарт-тега в документе. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype/) { get; } | ВозвратSmartTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Properties](../../aspose.words.markup/smarttag/properties/) { get; } | Коллекция свойств смарт-тегов. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Uri](../../aspose.words.markup/smarttag/uri/) { get; set; } | Указывает URI пространства имен смарт-тега. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.markup/smarttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца SmartTag. |
| override [AcceptStart](../../aspose.words.markup/smarttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала SmartTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все`SmartTag` узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) что соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Смарт-теги — это своего рода пользовательская разметка XML. Смарт-теги предоставляют возможность встраивания семантики, определяемой пользователем, в документ с помощью возможности предоставления базового пространства имен/имени для прогона или набора прогонов в документе.

`SmartTag` может быть ребенком[`Paragraph`](../../aspose.words/paragraph/) или другой`SmartTag` узел.

Полный список дочерних узлов, которые могут встречаться внутри смарт-тега, состоит из [`BookmarkStart`](../../aspose.words/bookmarkstart/) ,[`BookmarkEnd`](../../aspose.words/bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../../aspose.words/run/) ,[`SpecialChar`](../../aspose.words/specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`CommentRangeStart`](../../aspose.words/commentrangestart/) , [`CommentRangeEnd`](../../aspose.words/commentrangeend/) , `SmartTag`.

## Примеры

Показывает, как создавать смарт-теги.

```csharp
public void Create()
{
    Document doc = new Document();

    // Смарт-тег появляется в документе, в котором Microsoft Word распознает часть текста как некоторую форму данных,
    // например имя, дату или адрес, и преобразует его в гиперссылку, которая отображается подчеркиванием из фиолетовых точек.
    SmartTag smartTag = new SmartTag(doc);

    // Смарт-теги — это составные узлы, содержащие распознанный текст целиком.
    // Добавьте содержимое в этот смарт-тег вручную.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word может распознать указанное выше содержимое как дату.
    // Смарт-теги используют свойство «Элемент» для отражения типа содержащихся в них данных.
    smartTag.Element = "date";

    // Некоторые типы смарт-тегов дополнительно обрабатывают свое содержимое в пользовательские свойства XML.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Установите URI смарт-тега на значение по умолчанию.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Создайте еще один смарт-тег для биржевого тикера.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Распечатаем все смарт-теги в нашем документе с помощью посетителя документа.
    doc.Accept(new SmartTagPrinter());

    // Старые версии Microsoft Word поддерживают смарт-теги.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Используйте метод «RemoveSmartTags» для удаления всех смарт-тегов из документа.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Печатает посещённые смарт-теги и их содержимое.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Вызывается, когда в документе встречается узел SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посещение узла SmartTag завершено.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
