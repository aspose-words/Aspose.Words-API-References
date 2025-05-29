---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Math.MathObjectType, чтобы легко определять и управлять типами объектов Office Math для улучшенной обработки документов.
type: docs
weight: 4800
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
| OMathPara | `1` | Математический абзац или зона отображения математики, которая содержит один или несколькоOMath элементы, находящиеся в режиме отображения. |
| Accent | `2` | Функция ударения, состоящая из основы и комбинационного диакритического знака. |
| Bar | `3` | Функция Bar, состоящая из базового аргумента и черточки сверху или снизу. |
| BorderBox | `4` | Объект Border Box, состоящий из рамки, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения) |
| Box | `5` | Объект Box, который используется для группировки компонентов уравнения или другого экземпляра математического текста. |
| Delimiter | `6` | Объект-разделитель, состоящий из открывающих и закрывающих разделителей (таких как круглые скобки, фигурные скобки , квадратные скобки и вертикальные черты), а также элемента, содержащегося внутри. |
| Degree | `7` | Степень в математическом радикале. |
| Argument | `8` | Объект аргумента. Охватывает сущности Office Math, когда они используются в качестве аргументов для других сущностей Office Math. |
| Array | `9` | Объект массива, состоящий из одного или нескольких уравнений, выражений или других математических текстовых строк , которые могут быть выровнены по вертикали как единое целое относительно окружающего текста в строке. |
| Fraction | `10` | Объект дроби, состоящий из числителя и знаменателя, разделенных дробной чертой. |
| Denominator | `11` | Знаменатель дробного объекта. |
| Numerator | `12` | Числитель объекта дроби. |
| Function | `13` | Объект Function-Apply, состоящий из имени функции и элемента аргумента, над которым выполняется действие. |
| FunctionName | `14` | Имя функции. Например, имена функций sin и cos. |
| GroupCharacter | `15` | Объект Group-Character, состоящий из символа, нарисованного над или под текстом, часто с целью визуальной группировки элементов |
| Limit | `16` | Нижний пределLowerLimit объект и верхний пределUpperLimit функция. |
| LowerLimit | `17` | Объект нижнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно под ним. |
| UpperLimit | `18` | Объект верхнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно над ним. |
| Matrix | `19` | Матричный объект, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одном или нескольких столбцах. |
| MatrixRow | `20` | Одна строка матрицы. |
| NAry | `21` | N-арный объект, состоящий из n-арного объекта, основания (или операнда) и необязательных верхнего и нижнего пределов. |
| Phantom | `22` | Фантомный объект. |
| Radical | `23` | Радикальный объект, состоящий из радикала, базового элемента и необязательной степени . |
| SubscriptPart | `24` | Нижний индекс объекта, который может иметь нижний индекс part. |
| SuperscriptPart | `25` | Верхний индекс надстрочного объекта. |
| PreSubSuperscript | `26` | Объект Pre-Sub-Superscript, состоящий из базового элемента и нижнего и верхнего индекса, размещенных слева от базового элемента. |
| Subscript | `27` | Объект нижнего индекса, состоящий из базового элемента и уменьшенного скрипта, размещенного ниже и правее. |
| SubSuperscript | `28` | Объект надстрочного индекса, состоящий из базового элемента, уменьшенного шрифта, размещенного ниже и правее, и уменьшенного шрифта, размещенного выше и правее. |
| Supercript | `29` | Объект надстрочного индекса, состоящий из базового элемента и уменьшенного шрифта, размещенного выше и правее. |

## Примеры

Показывает, как распечатать структуру узлов каждого узла офисной математики в документе.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Когда мы заставляем составной узел принять посетителя документа, посетитель посещает принимающий узел,
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
    /// Получает простой текст документа, накопленный посетителем.
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
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко посетитель находится в дереве документа.
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
