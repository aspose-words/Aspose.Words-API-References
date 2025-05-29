---
title: FieldIncludeText.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: 探索 FieldIncludeText 编码属性，轻松管理文件中的数据编码。这项重要功能将增强您的数据处理能力！
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldincludetext/encoding/
---
## FieldIncludeText.Encoding property

获取或设置应用于引用文件中的数据的编码。

```csharp
public string Encoding { get; set; }
```

## 例子

展示如何创建 INCLUDETEXT 字段并设置其属性。

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 以下是两种使用 INCLUDETEXT 字段在本地文件系统中显示 XML 文件内容的方法。
    // 1 - 对 XML 文档执行 XSL 转换：
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - 使用 XPath 从 XML 文档中获取特定元素：
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// 使用文档生成器插入具有自定义属性的 INCLUDETEXT 字段。
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### 也可以看看

* class [FieldIncludeText](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
