---
title: BuiltInDocumentProperties.Pages
second_title: Aspose.Words for .NET API 参考
description: BuiltInDocumentProperties 财产. 表示文档中页数的估计值
type: docs
weight: 220
url: /zh/net/aspose.words.properties/builtindocumentproperties/pages/
---
## BuiltInDocumentProperties.Pages property

表示文档中页数的估计值。

```csharp
public int Pages { get; set; }
```

### 评论

Aspose.Words 在您调用时更新此属性[`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/).

### 例子

显示如何使用“内容”类别中的文档属性。

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // 通过使用内置属性，
    // 我们可以把word/page/character count等文档统计数据当作元数据，不用打开文档就可以看一眼
    // 通过右键单击 Windows 资源管理器中的文件并导航到属性 > 来访问这些属性详情 >内容
    // 如果我们想在文档中显示这些数据，我们可以使用 NUMPAGES、NUMWORDS、NUMCHARS 等字段。
    // 此外，这些值也可以在 Microsoft Word 中通过导航 File > 查看属性>高级属性 >统计数据
    // 页数：PageCount 属性实时显示页数，其值可以赋值给 Pages 属性

    // “Pages”属性存储文档的页数。 
    Assert.AreEqual(6, properties.Pages);

    // “Words”、“Characters”和“CharactersWithSpaces”内置属性还显示各种文档统计信息，
    // 但我们需要在整个文档上调用“UpdateWordCount”方法，然后才能期望它们包含准确的值。
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // 计算文档中的行数，然后将结果赋给“Lines”内置属性。
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // 将文档中的段落节点数分配给“段落”内置属性。
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // 通过“Bytes”内置属性估计我们文档的文件大小。
    Assert.AreEqual(20310, properties.Bytes);

    // 为我们的文档设置不同的模板，然后手动更新“模板”内置属性以反映此更改。
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // “ContentStatus”是一个描述性的内置属性。
    properties.ContentStatus = "Draft";

    // 保存后，“ContentType”内置属性将包含输出保存格式的 MIME 类型。
    Assert.AreEqual(string.Empty, properties.ContentType);

    // 如果文档包含链接，并且它们都是最新的，我们可以将“LinksUpToDate”属性设置为“true”。
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// 计算文档中的行数。
/// 在构造时遍历文档的布局实体树，
/// 计算也包含真实文本的“Line”类型的实体。
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../builtindocumentproperties/)
* 部件 [Aspose.Words](../../../)


