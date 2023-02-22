---
title: Enum MathObjectType
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Math.MathObjectType 枚举. 指定 Office Math 对象的类型
type: docs
weight: 3870
url: /zh/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

指定 Office Math 对象的类型。

```csharp
public enum MathObjectType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| OMath | `0` | 数学文本实例。 |
| OMathPara | `1` | 数学段落，或显示数学区域，包含一个或多个OMath处于显示模式的元素。 |
| Accent | `2` | 重音函数，由一个基础和一个组合变音符号组成。 |
| Bar | `3` | 条形函数，由一个基本参数和一个上划线或下划线组成。 |
| BorderBox | `4` | Border Box 对象，由围绕数学文本实例（例如公式或方程式）绘制的边框组成 |
| Box | `5` | Box 对象，用于对方程式或其他数学文本实例的组件进行分组。 |
| Delimiter | `6` | Delimiter 对象，由开始和结束分隔符（如圆括号、 大括号、方括号和竖线）以及包含在里面的一个元素组成。 |
| Degree | `7` | 数学部首中的度数。 |
| Argument | `8` | 参数对象。将 Office Math 实体用作其他 Office Math 实体的参数时将其括起来。 |
| Array | `9` | 数组对象，由一个或多个方程式、表达式或其他数学文本组成，运行 可以相对于行上的周围文本垂直对齐。 |
| Fraction | `10` | 分数对象，由分子和分母组成，由分数条分隔。 |
| Denominator | `11` | 分数对象的分母。 |
| Numerator | `12` | 分数对象的分子。 |
| Function | `13` | Function-Apply 对象，由函数名和作用的参数元素组成。 |
| FunctionName | `14` | 函数的名称。例如，函数名称为 sin 和 cos. |
| GroupCharacter | `15` | Group-Character 对象，由在文本上方或下方绘制的字符组成，通常 用于视觉上对项目进行分组 |
| Limit | `16` | 的下限LowerLimit对象和 的上限UpperLimit函数. |
| LowerLimit | `17` | 下限对象，由基线上的文本和紧挨其下方的缩小尺寸文本组成。 |
| UpperLimit | `18` | Upper-Limit 对象，由基线上的文本和紧接其上方的缩小尺寸文本组成。 |
| Matrix | `19` | 矩阵对象，由排列在一行或多行和一或多列中的一个或多个元素组成。 |
| MatrixRow | `20` | 矩阵的单行。 |
| NAry | `21` | N 元对象，由一个 N 元对象、一个基数（或操作数）以及可选的上限和下限组成。 |
| Phantom | `22` | 幻象对象。 |
| Radical | `23` | 部首对象，由部首、基本元素和可选度数组成。 |
| SubscriptPart | `24` | 可以有下标部分的对象的下标。 |
| SuperscriptPart | `25` | 上标对象的上标。 |
| PreSubSuperscript | `26` | Pre-Sub-Superscript 对象，它由一个基本元素和一个放置在基本元素左侧的下标和上标组成。 |
| Subscript | `27` | 下标对象，它由一个基本元素和一个位于右下方的缩小大小的脚本组成。 |
| SubSuperscript | `28` | 子上标对象，它由一个基本元素、一个位于右下方的缩小尺寸的脚本以及一个位于上方和右侧的缩小尺寸的脚本组成。 |
| Supercript | `29` | 上标对象，它由一个基本元素和一个位于右上方的缩小大小的脚本组成。 |

### 例子

显示如何打印文档中每个办公室数学节点的节点结构。

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // 当我们得到一个复合节点来接受一个文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历所有节点的子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历一个节点的子节点的非二叉树。
/// 以所有遇到的 OfficeMath 节点及其子节点的字符串形式创建一个映射。
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 OfficeMath 节点时调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问过 OfficeMath 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行添加到 StringBuilder 并根据访问者在文档树中的深度缩进。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Math](../../aspose.words.math/)
* 部件 [Aspose.Words](../../)


