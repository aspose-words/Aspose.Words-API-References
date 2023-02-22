---
title: SmartTag.Accept
second_title: Справочник по API Aspose.Words для .NET
description: SmartTag метод. Принимает посетителя.
type: docs
weight: 60
url: /ru/net/aspose.words.markup/smarttag/accept/
---
## SmartTag.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который будет посещать узлы. |

### Возвращаемое значение

Истинно, если все узлы были посещены; false, если DocumentVisitor остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

звонки[`VisitSmartTagStart`](../../../aspose.words/documentvisitor/visitsmarttagstart/) , затем звонит[`Accept`](../../../aspose.words/node/accept/)для всех дочерних узлов смарт-тега и вызовов[`VisitSmartTagEnd`](../../../aspose.words/documentvisitor/visitsmarttagend/) в конце.

### Примеры

Показывает, как создавать смарт-теги.

```csharp
public void Create()
{
    Document doc = new Document();

    // Смарт-тег появляется в документе, в котором Microsoft Word распознает часть своего текста как некую форму данных,
    // таких как имя, дата или адрес, и преобразует их в гиперссылку, которая подчеркнута фиолетовой пунктирной линией.
    SmartTag smartTag = new SmartTag(doc);

    // Смарт-теги — это составные узлы, содержащие полностью распознанный текст.
    // Добавляем содержимое в этот смарт-тег вручную.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word может распознать вышеуказанное содержимое как дату.
    // Смарт-теги используют свойство «Элемент», чтобы отразить тип содержащихся в них данных.
    smartTag.Element = "date";

    // Некоторые типы смарт-тегов преобразуют свое содержимое в пользовательские свойства XML.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Установите для URI смарт-тега значение по умолчанию.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Создайте еще один смарт-тег для бегущей строки.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Печатаем все смарт-теги в нашем документе с помощью посетителя документа.
    doc.Accept(new SmartTagPrinter());

    // Старые версии Microsoft Word поддерживают смарт-теги.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Используйте метод «RemoveSmartTags», чтобы удалить все смарт-теги из документа.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Выводит посещенные смарт-теги и их содержимое.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [SmartTag](../)
* пространство имен [Aspose.Words.Markup](../../smarttag/)
* сборка [Aspose.Words](../../../)


