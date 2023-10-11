---
title: Enum MathObjectType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Math.MathObjectType перечисление. Указывает тип объекта Office Math.
type: docs
weight: 4110
url: /ru/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Указывает тип объекта Office Math.

```csharp
public enum MathObjectType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| OMath | `0` | Экземпляр математического текста. |
| OMathPara | `1` | Математический параграф или отображаемая математическая зона, содержащая один или несколькоOMath элементы, находящиеся в режиме отображения. |
| Accent | `2` | Функция ударения, состоящая из основы и объединяющего диакритического знака. |
| Bar | `3` | Функция Bar, состоящая из базового аргумента и верхней или нижней черты. |
| BorderBox | `4` | Объект Border Box, состоящий из рамки, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения) |
| Box | `5` | Объект Box, который используется для группировки компонентов уравнения или другого экземпляра математического текста. |
| Delimiter | `6` | Объект-разделитель, состоящий из открывающих и закрывающих разделителей (таких как круглые скобки, фигурные скобки , квадратные скобки и вертикальные полосы) и элемента, содержащегося внутри. |
| Degree | `7` | Степень в математическом радикале. |
| Argument | `8` | Объект аргумента. Заключает объекты Office Math, когда они используются в качестве аргументов для других объектов Office Math. |
| Array | `9` | Объект массива, состоящий из одного или нескольких уравнений, выражений или другого математического текста, запускает , который можно выровнять по вертикали как единицу относительно окружающего текста в строке. |
| Fraction | `10` | Объект дроби, состоящий из числителя и знаменателя, разделенных чертой дроби. |
| Denominator | `11` | Знаменатель дробного объекта. |
| Numerator | `12` | Числитель объекта Fraction. |
| Function | `13` | Объект Function-Apply, который состоит из имени функции и элемента аргумента, на который воздействует. |
| FunctionName | `14` | Имя функции. Например, имена функций — sin и cos. . |
| GroupCharacter | `15` | Объект Group-Character, состоящий из символа, нарисованного над или под текстом, часто с целью визуальной группировки элементов |
| Limit | `16` | Нижний пределLowerLimit объект и верхний пределUpperLimit функция. |
| LowerLimit | `17` | Объект нижнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно под ней. |
| UpperLimit | `18` | Объект верхнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно над ней. |
| Matrix | `19` | Матричный объект, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одном или нескольких столбцах. |
| MatrixRow | `20` | Одна строка матрицы. |
| NAry | `21` | N-арный объект, состоящий из n-арного объекта, базового (или операнда) и необязательных верхнего и нижнего пределов. |
| Phantom | `22` | Фантомный объект. |
| Radical | `23` | Радикальный объект, состоящий из радикала, базового элемента и необязательной степени . |
| SubscriptPart | `24` | Индекс объекта, который может иметь индексную часть. |
| SuperscriptPart | `25` | Надстрочный индекс объекта надстрочного индекса. |
| PreSubSuperscript | `26` | Объект Pre-Sub-Superscript, который состоит из базового элемента, а также нижнего и верхнего индекса, расположенных слева от базового. |
| Subscript | `27` | Объект индекса, который состоит из базового элемента и скрипта уменьшенного размера, расположенного ниже и справа. |
| SubSuperscript | `28` | Объект поднадстрочного индекса, который состоит из базового элемента, сценария уменьшенного размера, расположенного ниже и справа, и сценария уменьшенного размера, расположенного выше и справа. |
| Supercript | `29` | Объект надстрочного индекса, который состоит из базового элемента и скрипта уменьшенного размера, расположенного сверху и справа. |

### Примеры

Показывает, как распечатать структуру каждого узла офисной математики в документе.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Когда мы получаем составной узел для приема посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит недвоичное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов OfficeMath и их дочерних элементов.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Получает открытый текст документа, накопленный посетителем.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку к StringBuilder и отступаем от нее в зависимости от того, насколько глубоко посетитель находится в дереве документа.
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

### Смотрите также

* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)


