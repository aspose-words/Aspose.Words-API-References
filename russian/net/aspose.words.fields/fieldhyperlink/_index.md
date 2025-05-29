---
title: FieldHyperlink Class
linktitle: FieldHyperlink
articleTitle: FieldHyperlink
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldHyperlink, который позволит легко реализовать поля HYPERLINK в ваших документах и повысить интерактивность.
type: docs
weight: 2400
url: /ru/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

Реализует поле HYPERLINK

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldHyperlink : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldHyperlink](fieldhyperlink/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address/) { get; set; } | Возвращает или задает место, куда переходит эта гиперссылка. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap/) { get; set; } | Возвращает или задает, следует ли добавлять координаты к гиперссылке для серверной карты изображений. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow/) { get; set; } | Возвращает или задает, следует ли открывать целевой сайт в новом окне веб-браузера. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip/) { get; set; } | Получает или задает текст всплывающей подсказки для гиперссылки. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress/) { get; set; } | Возвращает или задает местоположение в файле, например закладку, куда ведет эта гиперссылка. |
| [Target](../../aspose.words.fields/fieldhyperlink/target/) { get; set; } | Получает или задает цель, на которую должна быть перенаправлена ссылка. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

При выборе этого параметра элемент управления переходит к такому местоположению, как закладка или URL-адрес.

## Примеры

Показывает, как использовать поля HYPERLINK для ссылки на документы в локальной файловой системе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Когда мы нажимаем на это поле ГИПЕРССЫЛКА в Microsoft Word,
// откроется связанный документ, а затем курсор будет установлен на указанной закладке.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Когда мы нажимаем на это поле ГИПЕРССЫЛКА в Microsoft Word,
// откроется связанный документ и автоматически прокрутится вниз до указанного iframe.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
