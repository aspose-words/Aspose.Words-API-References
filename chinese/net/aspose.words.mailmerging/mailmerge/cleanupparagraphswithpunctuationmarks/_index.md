---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words for .NET API 参考
description: MailMerge 财产. 获取或设置一个值该值指示带标点符号的段落是否被视为空 并且如果RemoveEmptyParagraphs已指定选项
type: docs
weight: 20
url: /zh/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

获取或设置一个值，该值指示带标点符号的段落是否被视为空 ，并且如果RemoveEmptyParagraphs已指定选项。

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

### 评论

默认值为`真的`.

以下是可清除标点符号的完整列表：

* ！
* ,
* 。
* :
* ;
* ？
* ¡
* ¿

### 例子

演示如何在邮件合并操作后删除带有标点符号的段落。

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

// 将“CleanupParagraphsWithPunctuationMarks”属性设置为“true”也会对段落进行计数
// 标点符号为空，并将获得邮件合并操作来删除它们。
// 将“CleanupParagraphsWithPunctuationMarks”属性设置为“false”
// 将删除空段落，但不删除带有标点符号的段落。
// 这是该属性涉及的标点符号列表：“!”、“,”、“.”、“:”、“;”、“?”、“¡”、“¿”。
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


