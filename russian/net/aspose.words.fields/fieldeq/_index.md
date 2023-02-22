---
title: Class FieldEQ
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldEQ сорт. Реализует поле EQ.
type: docs
weight: 1680
url: /ru/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Реализует поле EQ.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примеры

Показывает, как использовать поле EQ для отображения различных математических уравнений.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // В поле EQ отображается математическое уравнение, состоящее из одного или нескольких элементов.
    // Каждый элемент имеет следующую форму: [переключатель][параметры][аргументы].
    // Переключатель может быть один, а возможных вариантов несколько.
    // Аргументы представляют собой набор значений, разделенных запятыми, заключенных в круглые скобки.

    // Здесь мы используем конструктор документов для вставки поля эквалайзера с переключателем "\f", который соответствует "Дробь".
    // Мы будем передавать значения 1 и 4 в качестве аргументов и не будем использовать никаких опций.
    // В этом поле будет отображаться дробь с 1 в числителе и 4 в знаменателе.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Одно поле EQ может содержать несколько элементов, размещенных последовательно.
    // Мы также можем вкладывать элементы друг в друга, помещая внутренние элементы
    // внутри скобок аргументов внешних элементов.
    // Мы можем найти полный список переключателей вместе с их использованием здесь:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // Ниже приведены приложения девяти различных переключателей полей эквалайзера, которые мы можем использовать для создания различных типов объектов.
    // 1 - Переключатель массива "\a", выровнен по левому краю, 2 столбца, 3 точки интервала по горизонтали и вертикали:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Переключатель скобок "\b", символ скобки "[", чтобы заключить содержимое в набор квадратных скобок:
    // Обратите внимание, что мы вкладываем в скобки массив, который на выходе будет выглядеть как матрица.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Переключатель смещения "\d", смещающий текст "B" на 30 пробелов справа от "A", отображая пробел в виде подчеркивания:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Формула, состоящая из нескольких дробей:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Интегральный переключатель "\i", с символом суммирования:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Переключатель списка "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Радикальный переключатель "\r", отображающий кубический корень из x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Переключатель нижнего/верхнего индекса "/s", сначала как верхний индекс, а затем как нижний индекс:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Переключатель поля "\x", с линиями сверху, снизу, слева и справа от ввода:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Еще несколько сложных комбинаций.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");

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


