---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldEQ 类，实现无缝 EQ 字段实现。通过强大的功能和灵活性增强文档自动化。
type: docs
weight: 2240
url: /zh/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

实现 EQ 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldEQ : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldEQ](fieldeq/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | 返回与 EQ 字段对应的 Office Math 对象。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 例子

展示如何用 Office Math 替换 EQ 字段。

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

展示如何使用 EQ 字段显示各种数学方程式。

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // EQ 字段显示由一个或多个元素组成的数学等式。
    // 每个元素采用以下形式：[switch][options][arguments]。
    // 可能有一个开关和几个可能的选项。
    // 参数是一组用圆括号括起来的逗号分隔的值。

    // 这里我们使用文档生成器插入一个 EQ 字段，带有“\f”开关，对应“分数”。
    // 我们将传递值 1 和 4 作为参数，并且不会使用任何选项。
    // 该字段将显示一个以 1 为分子、以 4 为分母的分数。
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // 一个 EQ 字段可能包含多个按顺序放置的元素。
    // 我们还可以通过放置内部元素来将元素嵌套在另一个元素中
    // 在外部元素的参数括号内。
    // 我们可以在这里找到开关的完整列表及其用途：
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // 下面是九种不同的 EQ 场开关的应用，我们可以使用它们来创建不同类型的对象。
    // 1 - 数组开关“\a”，左对齐，2 列，水平和垂直间距 3 点：
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - 括号开关“\b”，括号字符“[”，将内容括在方括号中：
    // 请注意，我们在括号内嵌套了一个数组，它在输出中看起来像一个矩阵。
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - 位移开关“\d”，将文本“B”位移至“A”右侧 30 个空格，并将间隙显示为下划线：
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - 由多个分数组成的公式：
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - 积分开关“\i”，带有求和符号：
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - 列表开关“\l”：
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - 根号开关“\r”，显示 x 的立方根：
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - 下标/上标开关“/s”，首先作为上标，然后作为下标：
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - 框开关“\x”，在输入的顶部、底部、左侧和右侧都有线：
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // 一些更复杂的组合。
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// 使用文档生成器插入 EQ 字段，设置其参数并开始新段落。
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
