---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeOptions 类，实现无缝低代码邮件合并解决方案。使用可自定义的功能增强您的文档自动化！
type: docs
weight: 4260
url: /zh/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

代表邮件合并功能的选项。

```csharp
public class MailMergeOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | 获取或设置一组标志，指定在邮件合并期间应删除哪些项目。 |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | 获取或设置一个值，指示带有标点符号的段落是否被视为空 ，并且如果RemoveEmptyParagraphs指定了选项。 |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | 获取或设置一个值，该值指示在执行针对数据源的区域邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域 ，还是仅合并第一个。 |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | 获取或设置一个值，该值指示在执行带有区域的邮件合并时是否更新整个文档中的字段。 |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | 获取或设置一个值，指示是否应保留未使用的“胡子”标签。 |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | 获取或设置邮件合并区域结束标签。 |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | 获取或设置邮件合并区域开始标记。 |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | 获取或设置一个值，指示执行邮件合并后列表是否在每个部分重新启动。 |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | 获取或设置一个值，该值指示第一个文档节的节开头及其后续数据源行的副本是否在邮件合并期间保留或根据 MS Word 行为进行更新。 |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | 获取或设置一个值，指示是否从邮件合并值中删除尾随和前导空格。 |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | 获取或设置一个值，该值指示合并字段和合并区域是否合并，而不管父 IF 字段的条件如何。 |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | 当`真的`，指定除了 MERGEFIELD 字段之外，邮件合并还会执行到一些其他类型的字段中，并且还会执行到“{{fieldName}}”标签中。 |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | 获取或设置一个值，指示整个段落是否**表开始**或者**桌尾**field 或之间的特定范围**表开始**和**桌尾**字段应包含在邮件合并区域中。 |

## 例子

展示如何对单个记录进行邮件合并操作。

```csharp
// 有几种方法可以进行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
