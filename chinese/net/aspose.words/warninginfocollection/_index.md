---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.WarningInfoCollection 班级. 表示类型化集合WarningInfo对象 在 C#.
type: docs
weight: 6640
url: /zh/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

表示类型化集合[`WarningInfo`](../warninginfo/)对象.

要了解更多信息，请访问[使用文档编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | 获取指定索引处的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | 从集合中删除所有元素。 |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | 实现[`IWarningCallback`](../iwarningcallback/)界面。向此集合添加警告。 |

## 评论

您可以将此集合对象用作最简单的形式[`IWarningCallback`](../iwarningcallback/)实现收集 Aspose.Words 在加载或保存操作期间生成的所有警告。创建此类的一个实例并将其分配给 [`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/)或者[`WarningCallback`](../documentbase/warningcallback/)财产。

## 例子

演示如何设置属性以从可用字体源中查找缺失字体的最接近匹配项。

```csharp
public void EnableFontSubstitution()
{
    // 打开一个文档，其中包含使用我们任何字体源中不存在的字体格式化的文本。
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// 每次加载/保存期间发生警告时调用。
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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
