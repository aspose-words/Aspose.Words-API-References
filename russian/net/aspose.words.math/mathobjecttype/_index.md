---
title: MathObjectType
second_title: Справочник по API Aspose.Words для .NET
description: Указывает тип объекта Office Math.
type: docs
weight: 3820
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
| OMathPara | `1` | Математический абзац или отображаемая математическая зона, содержащая один или несколько элементовOMathв режиме отображения. |
| Accent | `2` | Акцентная функция, состоящая из основы и объединяющего диакритического знака. |
| Bar | `3` | Функция полосы, состоящая из базового аргумента и верхней или нижней черты. |
| BorderBox | `4` | Объект Border Box, состоящий из границы, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения) |
| Box | `5` | Объект Box, который используется для группировки компонентов уравнения или другого экземпляра математического текста. |
| Delimiter | `6` | Объект-разделитель, состоящий из открывающих и закрывающих разделителей (таких как круглые скобки, фигурные скобки, квадратные скобки и вертикальные черты), и элемент, содержащийся внутри . |
| Degree | `7` | Степень математического радикала. |
| Argument | `8` | Объект аргумента. Закрывает объекты Office Math, когда они используются в качестве аргументов для других объектов Office Math. |
| Array | `9` | Объект массива, состоящий из одного или нескольких уравнений, выражений или другого математического текста , который может быть выровнен по вертикали как единое целое по отношению к окружающий текст в строке. |
| Fraction | `10` | Объект дроби, состоящий из числителя и знаменателя, разделенных чертой дроби. |
| Denominator | `11` | Знаменатель дробного объекта. |
| Numerator | `12` | Числитель объекта Fraction. |
| Function | `13` | Объект Function-Apply, который состоит из имени функции и элемента аргумента, на который воздействует. |
| FunctionName | `14` | Имя функции. Например, имена функций — sin и cos. |
| GroupCharacter | `15` | Объект Group-Character, состоящий из символа, нарисованного над или под текстом, часто с целью визуального группирования элементов |
| Limit | `16` | Нижний предел объектаLowerLimitи верхний предел функцииUpperLimit. |
| LowerLimit | `17` | Объект нижнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно под ним. |
| UpperLimit | `18` | Объект верхнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно над ним. |
| Matrix | `19` | Матричный объект, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одном или нескольких столбцах. |
| MatrixRow | `20` | Одна строка матрицы. |
| NAry | `21` | N-мерный объект, состоящий из n-мерного объекта, базы (или операнда) и необязательных верхнего и нижнего пределов. |
| Phantom | `22` | Фантомный объект. |
| Radical | `23` | Радикальный объект, состоящий из радикала, базового элемента и необязательной степени. |
| SubscriptPart | `24` | Нижний индекс объекта, который может иметь индексную часть. |
| SuperscriptPart | `25` | Верхний индекс надстрочного объекта. |
| PreSubSuperscript | `26` | Объект Pre-Sub-Superscript, который состоит из базового элемента и нижнего и верхнего индексов, расположенных слева от основания. |
| Subscript | `27` | Объект нижнего индекса, который состоит из базового элемента и скрипта уменьшенного размера, расположенного ниже и правее. |
| SubSuperscript | `28` | Поднадстрочный объект, состоящий из базового элемента, шрифта уменьшенного размера, расположенного ниже и правее, и скрипта уменьшенного размера, расположенного выше и Правильно. |
| Supercript | `29` | Надстрочный объект, который состоит из базового элемента и уменьшенного шрифта, расположенного сверху и справа. |

### Примеры

Показывает, как напечатать структуру узла каждого узла офисной математики в документе.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

     // Когда составной узел принимает посетителя документа, посетитель посещает принимающий узел, 
     // а затем обходит все дочерние узлы в порядке глубины.
     // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
 /// Обходит небинарное дерево дочерних узлов узла.
 /// Создает карту в виде строки всех встреченных узлов OfficeMath и их потомков.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
     /// Получает простой текст документа, который накопил посетитель.
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

* namespace [Aspose.Words.Math](../../aspose.words.math)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
