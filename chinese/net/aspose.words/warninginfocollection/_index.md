---
title: Class WarningInfoCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.WarningInfoCollection 班级. 表示一个类型化的集合WarningInfo对象.
type: docs
weight: 6330
url: /zh/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

表示一个类型化的集合[`WarningInfo`](../warninginfo/)对象.

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
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | 获取集合中包含的元素数。 |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | 获取指定索引处的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | 从集合中删除所有元素。 |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | 返回一个可用于迭代集合中所有项目的枚举器对象。 |
| [Warning](../../aspose.words/warninginfocollection/warning/)(WarningInfo) | 实现[`IWarningCallback`](../iwarningcallback/)界面。向此集合添加警告。 |

### 评论

您可以将此集合对象用作最简单的形式[`IWarningCallback`](../iwarningcallback/)实现收集 Aspose.Words 在加载或保存操作期间生成的所有警告。创建该类的一个实例并将其分配给 [`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/)或者[`WarningCallback`](../documentbase/warningcallback/)财产。

### 例子

演示如何设置属性以从可用字体源中查找缺失字体的最接近匹配项。

```csharp
[Test]
public void EnableFontSubstitution()
{
    // 打开一个文档，其中包含使用我们的任何字体源中都不存在的字体格式化的文本。
    Document doc = new Document(MyDir + "Missing font.docx");

    // 分配一个回调来处理字体替换警告。
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // 设置默认字体名称并启用字体替换。
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

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
    /// 在加载/保存过程中每次出现警告时调用。
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


