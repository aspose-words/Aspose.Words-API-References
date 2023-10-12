---
title: HtmlLoadOptions.WebRequestTimeout
second_title: Aspose.Words for .NET API 参考
description: HtmlLoadOptions 财产. Web 请求超时之前等待的毫秒数默认值为 100000 毫秒 100 秒.
type: docs
weight: 70
url: /zh/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Web 请求超时之前等待的毫秒数。默认值为 100000 毫秒 （100 秒）.

```csharp
public int WebRequestTimeout { get; set; }
```

### 评论

加载 HTML 和 MHTML 文档中链接的外部资源（图像、style 工作表）时，Aspose.Words 等待响应的毫秒数。

### 例子

演示如何在加载具有通过 URL 链接的外部资源的文档时设置 Web 请求的时间限制。

```csharp
public void WebRequestTimeout()
{
    // 创建一个新的 HtmlLoadOptions 对象并验证其 Web 请求的超时阈值。
    HtmlLoadOptions options = new HtmlLoadOptions();

    // 当加载带有通过网址 URL 外部链接的资源的 Html 文档时，
    // Aspose.Words 将中止未能在此时间限制（以毫秒为单位）内获取资源的 Web 请求。
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // 设置一个WarningCallback，它将记录加载期间发生的所有警告。
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // 加载这样的文档并验证是否已创建带有图像数据的形状。
    // 此链接图像需要网络请求才能加载，该请求必须在我们的时间限制内完成。
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // 设置不合理的超时限制并尝试再次加载文档。
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // 未能在时限内获取图像的Web请求仍然会产生图像。
    // 但是，图像将是红色“x”，通常表示缺少图像。
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // 我们还可以配置自定义回调来获取来自超时 Web 请求的任何警告。
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// 将文档加载操作期间发生的所有警告存储在列表中。
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

### 也可以看看

* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../htmlloadoptions/)
* 部件 [Aspose.Words](../../../)


