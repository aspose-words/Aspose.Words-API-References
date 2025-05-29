---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words for .NET
description: 使用 CleanupParagraphsWithPunctuationMarks 属性优化您的邮件合并功能。控制空段落的删除，使文档更简洁、更专业。
type: docs
weight: 20
url: /zh/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

获取或设置一个值，指示带有标点符号的段落是否被视为空 ，并且如果RemoveEmptyParagraphs指定了选项。

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## 评论

默认值为`真的`.

以下是可清除标点符号的完整列表：

* ！
* ，
* 。
* ：
* ；
* ？
* ¡
* ¿

## 例子

展示如何在邮件合并操作后删除带有标点符号的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// 配置“CleanupOptions”属性以删除此邮件合并将创建的任何空段落。
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// 将“CleanupParagraphsWithPunctuationMarks”属性设置为“true”也会计算段落
// 标点符号为空，并且将通过邮件合并操作将其删除。
// 将“CleanupParagraphsWithPunctuationMarks”属性设置为“false”
// 将删除空段落，但不会删除带有标点符号的段落。
// 这是该属性涉及的标点符号列表：“！”，“，”，“。”，“：”，“；”，“？”，“¡”，“¿”。
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
