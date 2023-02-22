---
title: CompositeNode.CreateNavigator
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode метод. Зарезервировано для системного использования. IXPathNavigable.
type: docs
weight: 80
url: /ru/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Зарезервировано для системного использования. IXPathNavigable.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Примеры

Показывает, как создать XPathNavigator, а затем использовать его для обхода и чтения узлов.

```csharp
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // В дереве документов есть документ, первая секция,
        // тело и первый абзац как узлы, каждый из которых является единственным дочерним элементом предыдущего.
        // Мы можем добавить еще несколько, чтобы дать дереву несколько ветвей, по которым может перемещаться навигатор.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Используйте наш навигатор, чтобы вывести карту всех узлов в документе на консоль.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
}

/// <summary>
/// Просматривает все дочерние элементы составного узла и отображает структуру в стиле дерева каталогов.
/// Величина отступа указывает глубину относительно начального узла.
/// Печатает текстовое содержимое текущего узла, только если это Run.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)


