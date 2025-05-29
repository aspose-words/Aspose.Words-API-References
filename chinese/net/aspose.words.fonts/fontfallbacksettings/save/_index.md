---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: 使用我们直观的“保存”方法，轻松保存您的 FontFallbackSettings。保留您的自定义后备设置，实现无缝字体管理。
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

将当前后备设置保存到流。

```csharp
public void Save(Stream outputStream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |

## 例子

展示如何从流中加载和保存字体回退设置。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 加载定义一组字体回退设置的 XML 文档。
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// 使用流将文档的当前字体回退设置保存为 XML 文档。
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### 也可以看看

* class [FontFallbackSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

将当前后备设置保存到文件。

```csharp
public void Save(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 输出文件名。 |

## 例子

展示如何从本地文件系统中的 XML 文档加载和保存字体回退设置。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 加载定义一组字体回退设置的 XML 文档。
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// 将我们文档的当前字体后备设置保存为 XML 文档。
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### 也可以看看

* class [FontFallbackSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
