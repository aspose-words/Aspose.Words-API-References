---
title: BorderCollection.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: BorderCollection 方法. 返回一个枚举器对象可用于迭代集合中的所有边框
type: docs
weight: 160
url: /zh/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

返回一个枚举器对象，可用于迭代集合中的所有边框。

```csharp
public IEnumerator<Border> GetEnumerator()
```

### 例子

演示如何迭代和编辑段落格式对象中的所有边框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 配置构建器的段落格式设置以在所有侧面创建绿色波浪边框。
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// 插入一个段落。我们的边框设置将决定其边框的外观。
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### 也可以看看

* class [Border](../../border/)
* class [BorderCollection](../)
* 命名空间 [Aspose.Words](../../bordercollection/)
* 部件 [Aspose.Words](../../../)


