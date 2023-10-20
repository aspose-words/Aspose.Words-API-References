---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words для .NET
description: DocumentBuilder InsertCheckBox метод. Вставляет поле формы флажка в текущую позицию на С#.
type: docs
weight: 290
url: /ru/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Вставляет поле формы флажка в текущую позицию.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет обрезано. |
| checkedValue | Boolean | Проверено состояние поля формы флажка. |
| size | Int32 | Определяет размер флажка в пунктах. Укажите 0 для MS Word , чтобы автоматически рассчитать размер флажка. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если вы укажете имя для поля формы, то автоматически создастся закладка с таким же именем.

## Примеры

Показывает, как вставлять флажки в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем флажки разных размеров и отмеченных статусов по умолчанию.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Поля формы имеют ограничение на длину имени в 20 символов.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щелкнув их.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Смотрите также

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Вставляет поле формы флажка в текущую позицию.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет обрезано. |
| defaultValue | Boolean | Значение по умолчанию поля формы флажка. |
| checkedValue | Boolean | Текущий проверенный статус поля формы флажка. |
| size | Int32 | Определяет размер флажка в пунктах. Укажите 0 для MS Word , чтобы автоматически рассчитать размер флажка. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если вы укажете имя для поля формы, то автоматически создастся закладка с таким же именем.

## Примеры

Показывает, как вставлять флажки в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем флажки разных размеров и отмеченных статусов по умолчанию.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Поля формы имеют ограничение на длину имени в 20 символов.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щелкнув их.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Смотрите также

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
