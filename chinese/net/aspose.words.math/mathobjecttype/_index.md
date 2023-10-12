---
title: Enum MathObjectType
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Math.MathObjectType 枚举. 指定 Office Math 对象的类型
type: docs
weight: 4110
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
| OMathPara | `1` | 数学段落或显示数学区域，包含一个或多个OMath处于显示模式的元素。 |
| Accent | `2` | 重音函数，由基数和组合变音标记组成。 |
| Bar | `3` | Bar 函数，由基本参数和上划线或下划线组成。 |
| BorderBox | `4` | 边框框对象，由围绕数学文本实例（例如公式或方程）绘制的边框组成 |
| Box | `5` | Box 对象，用于对方程或数学文本的其他实例的组件进行分组。 |
| Delimiter | `6` | Delimiter 对象，由左右分隔符（如圆括号、 大括号、中括号和竖线）以及内部包含的元素组成。 |
| Degree | `7` | 数学根式的度数。 |
| Argument | `8` | 参数对象。当 Office Math 实体用作其他 Office Math 实体的参数时，将它们括起来。 |
| Array | `9` | 数组对象，由一个或多个方程、表达式或其他数学文本组成，运行 ，可以相对于行上的周围文本作为一个单元进行垂直对齐。 |
| Fraction | `10` | 分数对象，由由分数条分隔的分子和分母组成。 |
| Denominator | `11` | 分数对象的分母。 |
| Numerator | `12` | Fraction 对象的分子。 |
| Function | `13` | 函数应用对象，由函数名称和作用的参数元素组成。 |
| FunctionName | `14` | 函数的名称。例如，函数名称为 sin 和 cos. |
| GroupCharacter | `15` | 组字符对象，由在文本上方或下方绘制的字符组成，通常 目的是对项目进行可视分组 |
| Limit | `16` | 的下限LowerLimit对象和 的上限UpperLimit函数. |
| LowerLimit | `17` | 下限对象，由基线上的文本和紧邻其下方的缩小尺寸文本组成。 |
| UpperLimit | `18` | 上限对象，由基线上的文本和紧邻其上方的缩小尺寸文本组成。 |
| Matrix | `19` | 矩阵对象，由排列在一行或多行和一列或多列中的一个或多个元素组成。 |
| MatrixRow | `20` | 矩阵的单行。 |
| NAry | `21` | N 元对象，由一个 n 元对象、一个基数（或操作数）和可选的上限和下限组成。 |
| Phantom | `22` | 幻影对象。 |
| Radical | `23` | 部首对象，由部首、基本元素和可选度数组成。 |
| SubscriptPart | `24` | 可以有下标部分的对象的下标。 |
| SuperscriptPart | `25` | 上标对象的上标。 |
| PreSubSuperscript | `26` | Pre-Sub-Superscript 对象，由一个基本元素以及放置在该基本元素左侧的下标和上标组成。 |
| Subscript | `27` | 下标对象，由基本元素和位于右下方的缩小尺寸脚本组成。 |
| SubSuperscript | `28` | 子上标对象，由基本元素、位于下方和右侧的缩小尺寸脚本以及位于上方和右侧的缩小尺寸脚本组成。 |
| Supercript | `29` | 上标对象，由基本元素和位于上方和右侧的缩小尺寸脚本组成。 |

### 例子

演示如何打印文档中每个 Office Math 节点的节点结构。

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点的非二叉树。
/// 以字符串形式创建所有遇到的 OfficeMath 节点及其子节点的映射。
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
    /// 在访问 OfficeMath 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行追加到 StringBuilder 并根据访问者在文档树中的深度对其进行缩进。
    /// </summary>
    /// <param name="text"></param>;
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


