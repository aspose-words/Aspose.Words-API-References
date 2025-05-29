---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words for .NET
description: 探索 HtmlLoadOptions 的 WebRequestTimeout 属性，它允许您自定义超时设置以获得最佳 Web 性能。默认值为 100 秒。
type: docs
weight: 80
url: /zh/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Web 请求超时前等待的毫秒数。默认值为 100000 毫秒 （100 秒）。

```csharp
public int WebRequestTimeout { get; set; }
```

## 评论

加载 HTML 和 MHTML 文档中链接的外部资源（图像、style 表）时，Aspose.Words 等待响应的毫秒数。

## 例子

展示如何在加载包含通过 URL 链接的外部资源的文档时设置 Web 请求的时间限制。

```csharp
public void WebRequestTimeout()
{
    // 创建一个新的 HtmlLoadOptions 对象并验证其 Web 请求的超时阈值。
    HtmlLoadOptions options = new HtmlLoadOptions();

    // 当加载一个包含通过网址 URL 进行外部链接的资源的 Html 文档时，
    // Aspose.Words 将中止在该时间限制内（以毫秒为单位）无法获取资源的 Web 请求。
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // 设置一个WarningCallback，它将记录加载期间发生的所有警告。
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // 加载这样的文档并验证是否已创建具有图像数据的形状。
    // 此链接图像将需要网络请求来加载，并且必须在我们的时间限制内完成。
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // 设置不合理的超时限制并再次尝试加载文档。
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // 在限定时间内未能获取图像的网页请求仍然会产生图像。
    // 但是，图像将是红色的“x”，通常表示缺少图像。
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // 我们还可以配置自定义回调来获取超时 Web 请求的任何警告。
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
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
