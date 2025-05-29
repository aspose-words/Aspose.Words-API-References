---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words для .NET
description: С легкостью копируйте стили из выбранного шаблона в любой документ с помощью метода CopyStylesFromTemplate, улучшая рабочий процесс и обеспечивая единообразие документа.
type: docs
weight: 610
url: /ru/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

Копирует стили из указанного шаблона в документ.

```csharp
public void CopyStylesFromTemplate(string template)
```

## Примечания

Когда стили копируются из шаблона в документ, одноименные стили в документе переопределяются для соответствия описаниям стилей в шаблоне. Уникальные стили из шаблона копируются в документ. Уникальные стили в документе остаются нетронутыми.

## Примеры

Показывает, как копировать стили из одного документа в другой.

```csharp
// Создаем документ, а затем добавляем стили, которые будем копировать в другой документ.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Создаем документ, в который будем копировать стили.
Document target = new Document();

// Создаем стиль с тем же именем, что и стиль из шаблона документа, и добавляем его в целевой документ.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Существует два способа вызова метода для копирования всех стилей из одного документа в другой.
// 1 - Передача объекта шаблона документа:
target.CopyStylesFromTemplate(template);

// Копирование стилей добавляет все стили из шаблона документа в целевой
// и перезаписывает существующие стили с тем же именем.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Передача имени файла локальной системы шаблона документа:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

Копирует стили из указанного шаблона в документ.

```csharp
public void CopyStylesFromTemplate(Document template)
```

## Примечания

Когда стили копируются из шаблона в документ, одноименные стили в документе переопределяются для соответствия описаниям стилей в шаблоне. Уникальные стили из шаблона копируются в документ. Уникальные стили в документе остаются нетронутыми.

## Примеры

Показывает, как копировать стили из шаблона в документ через Document.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Показывает, как копировать стили из одного документа в другой.

```csharp
// Создаем документ, а затем добавляем стили, которые будем копировать в другой документ.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Создаем документ, в который будем копировать стили.
Document target = new Document();

// Создаем стиль с тем же именем, что и стиль из шаблона документа, и добавляем его в целевой документ.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Существует два способа вызова метода для копирования всех стилей из одного документа в другой.
// 1 - Передача объекта шаблона документа:
target.CopyStylesFromTemplate(template);

// Копирование стилей добавляет все стили из шаблона документа в целевой
// и перезаписывает существующие стили с тем же именем.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Передача имени файла локальной системы шаблона документа:
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
