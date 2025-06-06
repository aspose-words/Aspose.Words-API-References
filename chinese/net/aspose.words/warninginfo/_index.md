---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.WarningInfo 类，它提供有关文档加载或保存期间警告的重要见解，从而提高您的工作流程效率。
type: docs
weight: 7480
url: /zh/net/aspose.words/warninginfo/
---
## WarningInfo class

包含有关 Aspose.Words 在文档加载或保存期间发出的警告的信息。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class WarningInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | 返回警告的描述。 |
| [Source](../../aspose.words/warninginfo/source/) { get; } | 返回警告的来源。 |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | 返回警告的类型。 |

## 评论

您无需创建此类的实例。此类的对象已创建 ，并由 Aspose.Words 传递给[`Warning`](../iwarningcallback/warning/)方法。

## 例子

展示如何设置属性以从可用的字体源中查找与缺失字体最接近的匹配项。

```csharp
public void EnableFontSubstitution()
{
    // 打开包含使用我们任何字体源中都不存在的字体格式化的文本的文档。
    Document doc = new Document(MyDir + "Missing font.docx");

    // 分配一个回调来处理字体替换警告。
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // 设置默认字体名称并启用字体替换。
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // 字体替换后应使用原始字体规格。
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // 如果我们保存缺少字体的文档，我们将收到字体替换警告。
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // 我们还可以验证集合中的警告并清除它们。
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// 每次加载/保存期间出现警告时调用。
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
