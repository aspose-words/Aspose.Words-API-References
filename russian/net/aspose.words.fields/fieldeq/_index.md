---
title: Class FieldEQ
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldEQ сорт. Реализует поле эквалайзера.
type: docs
weight: 1830
url: /ru/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Реализует поле эквалайзера.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class FieldEQ : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldEQ](fieldeq/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | Возвращает объект Office Math, соответствующий полю EQ. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примеры

Показывает, как заменить поле EQ на Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Показывает, как использовать поле EQ для отображения различных математических уравнений.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Поле EQ отображает математическое уравнение, состоящее из одного или нескольких элементов.
    // Каждый элемент имеет следующий вид: [переключатель][опции][аргументы].
    // Переключатель может быть один, а возможных вариантов - несколько.
    // Аргументы представляют собой набор значений, разделенных запятыми, заключенных в круглые скобки.

    // Здесь мы используем конструктор документов для вставки поля EQ с переключателем «\f», который соответствует «Дроби».
    // Мы передадим значения 1 и 4 в качестве аргументов и не будем использовать какие-либо параметры.
    // В этом поле будет отображаться дробь с 1 в числителе и 4 в знаменателе.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Одно поле EQ может содержать несколько элементов, расположенных последовательно.
    // Мы также можем вкладывать элементы друг в друга, помещая внутренние элементы
    // внутри скобок аргументов внешних элементов.
    // Полный список переключателей и их использование можно найти здесь:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // Ниже приведены применения девяти различных переключателей полей эквалайзера, которые мы можем использовать для создания различных типов объектов.
    // 1 - переключатель массива "\a", выравнивание по левому краю, 2 столбца, 3 точки горизонтального и вертикального интервала:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - переключатель скобок "\b", символ скобки "[", чтобы заключить содержимое в набор квадратных скобок:
    // Обратите внимание, что мы вкладываем в скобки массив, который на выходе будет выглядеть как матрица.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Переключатель смещения "\d", смещающий текст "B" на 30 пробелов вправо от "A", отображающий пробел в виде подчеркивания:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Формула, состоящая из нескольких дробей:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Интегральный переключатель "\i", с символом суммирования:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Переключатель списка "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Радикальный переключатель "\r", отображающий кубический корень из x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Переключатель нижнего/надстрочного индекса "/s", сначала как верхний индекс, а затем как нижний индекс:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 — переключатель поля «\x», со строками вверху, внизу, слева и справа от ввода:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Еще несколько более сложных комбинаций.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Используйте конструктор документов, чтобы вставить поле EQ, установить его аргументы и начать новый абзац.
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

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


