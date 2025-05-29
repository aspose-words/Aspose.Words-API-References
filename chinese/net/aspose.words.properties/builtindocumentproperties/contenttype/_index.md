---
title: BuiltInDocumentProperties.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words for .NET
description: 了解如何使用 BuiltInDocumentProperties ContentType 属性来有效地管理文档的内容类型，以增强组织能力。
type: docs
weight: 90
url: /zh/net/aspose.words.properties/builtindocumentproperties/contenttype/
---
## BuiltInDocumentProperties.ContentType property

获取或设置文档的内容类型。

```csharp
public string ContentType { get; set; }
```

## 例子

展示如何使用“内容”类别中的文档属性。

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // 通过使用内置属性，
    // 我们可以将文档统计信息（例如字数/页数/字符数）视为元数据，无需打开文档即可查看
    // 可以通过在 Windows 资源管理器中右键单击文件并导航至“属性”>“详细信息”>“内容”来访问这些属性
    // 如果我们想在文档中显示这些数据，我们可以使用诸如 NUMPAGES、NUMWORDS、NUMCHARS 等字段。
    // 此外，您也可以在 Microsoft Word 中通过导航“文件”>“属性”>“高级属性”>“统计信息”来查看这些值
    // 页数：PageCount 属性实时显示页数，其值可以赋给 Pages 属性

    // “Pages”属性存储文档的页数。
    Assert.AreEqual(6, properties.Pages);

    // “Words”、“Characters”和“CharactersWithSpaces”内置属性还显示各种文档统计信息，
    // 但我们需要对整个文档调用“UpdateWordCount”方法，然后才能期望它们包含准确的值。
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

    // 通过“字节”内置属性获取文档文件大小的估计值。
    Assert.AreEqual(20310, properties.Bytes);

    // 为我们的文档设置不同的模板，然后手动更新“模板”内置属性以反映此更改。
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // “ContentStatus” 是一个描述性的内置属性。
    properties.ContentStatus = "Draft";

    // 保存后，“ContentType”内置属性将包含输出保存格式的 MIME 类型。
    Assert.AreEqual(string.Empty, properties.ContentType);

    // 如果文档包含链接，并且它们都是最新的，我们可以将“LinksUpToDate”属性设置为“true”。
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// 计算文档中的行数。
/// 在构建时遍历文档的布局实体树，
/// 计算也包含真实文本的“线”类型的实体。
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
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
