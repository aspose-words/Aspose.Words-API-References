---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words для .NET
description: С легкостью добавляйте интерактивные поля флажков с помощью метода InsertCheckBox в DocumentBuilder, повышая вовлеченность пользователей в ваши документы.
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
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет усечено. |
| checkedValue | Boolean | Проверен статус поля формы флажка. |
| size | Int32 | Указывает размер флажка в пунктах. Укажите 0 для MS Word , чтобы автоматически рассчитать размер флажка. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если указать имя поля формы, то автоматически будет создана закладка с таким же именем.

## Примеры

Показывает, как вставлять флажки в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте флажки разных размеров и статусы по умолчанию.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Длина имени поля формы ограничена 20 символами.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щелкнув по ним.
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
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет усечено. |
| defaultValue | Boolean | Значение по умолчанию для поля формы флажка. |
| checkedValue | Boolean | Текущий отмеченный статус поля формы флажка. |
| size | Int32 | Указывает размер флажка в пунктах. Укажите 0 для MS Word , чтобы автоматически рассчитать размер флажка. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если указать имя поля формы, то автоматически будет создана закладка с таким же именем.

## Примеры

Показывает, как вставлять флажки в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте флажки разных размеров и статусы по умолчанию.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Длина имени поля формы ограничена 20 символами.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Мы можем взаимодействовать с этими флажками в Microsoft Word, дважды щелкнув по ним.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Смотрите также

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
