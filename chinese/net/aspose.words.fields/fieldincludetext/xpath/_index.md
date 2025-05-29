---
title: FieldIncludeText.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words for .NET
description: 发现 FieldIncludeText XPath 属性可以轻松访问和修改特定的 XML 部分，从而提高数据管理效率。
type: docs
weight: 90
url: /zh/net/aspose.words.fields/fieldincludetext/xpath/
---
## FieldIncludeText.XPath property

获取或设置 XML 文件所需部分的 XPath。

```csharp
public string XPath { get; set; }
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
