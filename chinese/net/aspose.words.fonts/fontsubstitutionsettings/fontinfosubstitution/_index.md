---
title: FontSubstitutionSettings.FontInfoSubstitution
linktitle: FontInfoSubstitution
articleTitle: FontInfoSubstitution
second_title: Aspose.Words for .NET
description: 了解 FontSubstitutionSettings 如何使用可自定义的字体信息规则来增强您的排版，从而改善设计和可读性。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/
---
## FontSubstitutionSettings.FontInfoSubstitution property

与字体信息替换规则相关的设置。

```csharp
public FontInfoSubstitutionRule FontInfoSubstitution { get; }
```

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

* class [FontInfoSubstitutionRule](../../fontinfosubstitutionrule/)
* class [FontSubstitutionSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
