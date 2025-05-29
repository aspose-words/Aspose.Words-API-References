---
title: FieldSeq.ResetNumber
linktitle: ResetNumber
articleTitle: ResetNumber
second_title: Aspose.Words for .NET
description: 轻松管理您的 FieldSeq ResetNumber 属性！设置或检索整数来控制序列号，确保数据处理的准确性。
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldseq/resetnumber/
---
## FieldSeq.ResetNumber property

获取或设置一个整数，用于重置序列号。如果该数字不存在，则返回 -1。

```csharp
public string ResetNumber { get; set; }
```

## 例子

显示使用 SEQ 字段创建的编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 插入一个 SEQ 字段，用于显示“MySequence”的当前计数值，
// 使用“ResetNumber”属性将其设置为 100 之后。
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// 使用另一个 SEQ 字段显示此序列中的下一个数字。
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 插入 1 级标题。
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// 从同一序列插入另一个 SEQ 字段，并将其配置为在每个标题处将计数重置为 1。
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// 上述标题是 1 级标题，因此该序列的计数重置为 1。
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// 移动到此序列的下一个数字。
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

### 也可以看看

* class [FieldSeq](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
