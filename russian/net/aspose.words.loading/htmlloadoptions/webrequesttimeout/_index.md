---
title: HtmlLoadOptions.WebRequestTimeout
second_title: Справочник по API Aspose.Words для .NET
description: HtmlLoadOptions свойство. Число миллисекунд ожидания до истечения времени ожидания вебзапроса. Значение по умолчанию  100000 миллисекунд 100 секунд. .
type: docs
weight: 70
url: /ru/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Число миллисекунд ожидания до истечения времени ожидания веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). .

```csharp
public int WebRequestTimeout { get; set; }
```

### Примечания

Количество миллисекунд, в течение которых Aspose.Words ожидает ответа при загрузке внешних ресурсов (изображений, листов style ), связанных в документах HTML и MHTML.

### Примеры

Показывает, как установить ограничение по времени для веб-запросов при загрузке документа с внешними ресурсами, связанными URL-адресами.

```csharp
public void WebRequestTimeout()
{
    // Создайте новый объект HtmlLoadOptions и проверьте его пороговое значение времени ожидания для веб-запроса.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // При загрузке HTML-документа с ресурсами, внешними ссылками по URL-адресу веб-адреса,
    // Aspose.Words прервет веб-запросы, которым не удалось получить ресурсы в течение этого срока (в миллисекундах).
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Установите alertCallback, который будет записывать все предупреждения, возникающие во время загрузки.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Загрузите такой документ и убедитесь, что создана фигура с данными изображения.
    // Для загрузки этого связанного изображения потребуется веб-запрос, который должен быть выполнен в течение установленного нами срока.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Установите необоснованный лимит времени ожидания и попробуйте загрузить документ еще раз.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Веб-запрос, которому не удалось получить изображение в течение установленного срока, все равно создаст изображение.
    // Однако на изображении будет красный крестик, который обычно означает отсутствие изображения.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Мы также можем настроить собственный обратный вызов для получения любых предупреждений от веб-запросов с истекшим временем ожидания.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Сохраняет все предупреждения, возникающие во время операции загрузки документа, в списке.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Смотрите также

* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../htmlloadoptions/)
* сборка [Aspose.Words](../../../)


