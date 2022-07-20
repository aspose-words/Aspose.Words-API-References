---
title: FieldListNum
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле LISTNUM.
type: docs
weight: 1970
url: /ru/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Реализует поле LISTNUM.

```csharp
public class FieldListNum : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldListNum](fieldlistnum)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname) { get; } | Возвращает значение, указывающее, предоставлено ли имя определения абстрактной нумерации кодом поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel) { get; set; } | Получает или задает уровень в списке, переопределяя поведение поля по умолчанию. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname) { get; set; } | Получает или задает имя определения абстрактной нумерации, используемого для нумерации. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber) { get; set; } | Получает или задает начальное значение для этого поля. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примеры

Показывает, как нумеровать абзацы с полями LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// В полях LISTNUM отображается число, которое увеличивается в каждом поле LISTNUM.
// Эти поля также имеют различные параметры, которые позволяют нам использовать их для эмуляции нумерованных списков.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// По умолчанию списки начинают считать с 1, но мы можем установить для этого числа другое значение, например 0.
// В этом поле будет отображаться «0)».
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // Поля LISTNUM поддерживают отдельные счетчики для каждого уровня списка.
// Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
// увеличивает уровень списка вместо количества.
// Следующее поле продолжит счет, который мы начали выше, и отобразит значение «1» на уровне списка 1.
builder.InsertField(FieldType.FieldListNum, true);

// Это поле начнет отсчет на уровне списка 2. Оно будет отображать значение «1».
builder.InsertField(FieldType.FieldListNum, true);

// Это поле начнет отсчет на уровне списка 3. Оно будет отображать значение «1».
// Разные уровни списка имеют разное форматирование,
// таким образом, эти поля вместе будут отображать значение "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Следующее поле LISTNUM, которое мы вставляем, продолжит подсчет на уровне списка
// что предыдущее поле LISTNUM было включено.
// Мы можем использовать свойство "ListLevel" для перехода на другой уровень списка.
// Если бы это поле LISTNUM оставалось на уровне списка 3, оно отображало бы "ii)",
// но поскольку мы переместили его на уровень списка 2, он продолжает считать на этом уровне и отображает "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Мы можем установить свойство ListName, чтобы заставить поле эмулировать другой тип поля AUTONUM.
// "NumberDefault" эмулирует AUTONUM, "OutlineDefault" эмулирует AUTONUMOUT,
// и «LegalDefault» эмулирует поля AUTONUMLGL.
// Имя списка "OutlineDefault" с 1 в качестве начального номера приведет к отображению "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Имя списка не переносится из предыдущего поля, поэтому нам нужно будет устанавливать его для каждого нового поля.
// Это поле продолжает счет с другим именем списка и отображает «II.».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
