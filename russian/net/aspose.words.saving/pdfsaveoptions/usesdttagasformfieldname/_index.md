---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PdfSaveOptions UseSdtTagAsFormFieldName улучшает формы PDF, используя теги управления SDT для лучшей организации и ясности.
type: docs
weight: 340
url: /ru/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Указывает, следует ли использовать тег элемента управления SDT или свойство Id в качестве имени поля формы в PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

При установке на`ЛОЖЬ`Свойство идентификатора элемента управления SDT используется в качестве имени поля формы в PDF.

При установке на`истинный`, Свойство тега элемента управления SDT используется в качестве имени поля формы в PDF.

Если установлено значение`истинный` и тег пуст, свойство Id будет использоваться в качестве имени поля формы.

Если установлено значение`истинный` и Значения тегов не являются уникальными, дублирующиеся значения тегов будут изменены на build уникальные имена полей формы PDF.

## Примеры

Показывает, как использовать свойство тега или идентификатора элемента управления SDT в качестве имени поля формы в PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// Если задано значение «false», свойство идентификатора элемента управления SDT используется как имя поля формы в PDF.
// Если задано значение «true», свойство тега элемента управления SDT используется как имя поля формы в PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
