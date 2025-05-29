---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Math.MathObjectType 枚举，轻松识别和管理 Office Math 对象类型，从而增强文档处理。
type: docs
weight: 4800
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
| Accent | `2` | 重音功能，由一个基数和一个组合变音符号组成。 |
| Bar | `3` | 条形函数，由一个基本参数和一个上划线或下划线组成。 |
| BorderBox | `4` | 边框框对象，由围绕数学文本实例（例如公式或方程式）绘制的边框组成 |
| Box | `5` | Box 对象，用于对方程式或其他数学文本实例的组成部分进行分组。 |
| Delimiter | `6` | 分隔符对象，由开始和结束分隔符（例如圆括号、 大括号、方括号和竖线）以及其中包含的元素组成。 |
| Degree | `7` | 数学根式的度数。 |
| Argument | `8` | 参数对象。当 Office Math 实体用作其他 Office Math 实体的参数时，将其括起来。 |
| Array | `9` | 数组对象，由一个或多个方程式、表达式或其他数学文本运行组成 ，可以作为一个单元相对于行上的周围文本垂直对齐。 |
| Fraction | `10` | 分数对象，由分数线分隔的分子和分母组成。 |
| Denominator | `11` | 分数对象的分母。 |
| Numerator | `12` | 分数对象的分子。 |
| Function | `13` | Function-Apply 对象，由函数名称和所作用的参数元素组成。 |
| FunctionName | `14` | 函数名称。例如，函数名称为 sin 和 cos。 |
| GroupCharacter | `15` | 组字符对象，由在文本上方或下方绘制的字符组成，通常为 ，目的是在视觉上对项目进行分组 |
| Limit | `16` | 下限LowerLimit对象和 的上限UpperLimit函数. |
| LowerLimit | `17` | Lower-Limit 对象，由基线上的文本和其正下方的缩小尺寸文本组成。 |
| UpperLimit | `18` | 上限对象，由基线上的文本和其正上方的缩小尺寸文本组成。 |
| Matrix | `19` | 矩阵对象，由一行或多行以及一列或多列中的一个或多个元素组成。 |
| MatrixRow | `20` | 矩阵的单行。 |
| NAry | `21` | N 元对象，由一个 n 元对象、一个基数（或操作数）以及可选的上限和下限组成。 |
| Phantom | `22` | 幻影对象. |
| Radical | `23` | 根式对象，由根式、基元和可选度数组成。 |
| SubscriptPart | `24` | 可以有下标部分的对象的下标。 |
| SuperscriptPart | `25` | 上标对象的上标。 |
| PreSubSuperscript | `26` | Pre-Sub-Superscript 对象，由一个基数元素以及位于基数左侧的下标和上标组成。 |
| Subscript | `27` | 下标对象，由一个基本元素和一个位于右下方的缩小尺寸脚本组成。 |
| SubSuperscript | `28` | 子上标对象，由一个基本元素、一个位于右下方的缩小尺寸脚本和一个位于右上方的缩小尺寸脚本组成。 |
| Supercript | `29` | 上标对象，由一个基本元素和一个位于右上方的缩小尺寸脚本组成。 |

## 例子

展示如何打印文档中每个办公数学节点的节点结构。

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者会访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点非二叉树。
/// 以字符串的形式创建所有遇到的 OfficeMath 节点及其子节点的映射。
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
    /// 当在文档中遇到 OfficeMath 节点时调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完 OfficeMath 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 附加一行并根据访问者在文档树中的深度进行缩进。
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
