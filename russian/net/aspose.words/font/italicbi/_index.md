---
title: Font.ItalicBi
linktitle: ItalicBi
articleTitle: ItalicBi
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ItalicBi для шрифтов, улучшите форматирование текста справа налево с помощью курсивных стилей для улучшения читаемости и привлекательности дизайна.
type: docs
weight: 170
url: /ru/net/aspose.words/font/italicbi/
---
## Font.ItalicBi property

True, если текст, написанный справа налево, отформатирован курсивом.

```csharp
public bool ItalicBi { get; set; }
```

## Примеры

Показывает, как задать отдельные наборы настроек шрифта для текста с письмом справа налево и справа налево.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Определить набор настроек шрифта для текста слева направо.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Определим другой набор настроек шрифта для текста, написанного справа налево.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Мы можем использовать флаг Bidi, чтобы указать, будет ли текст, который мы собираемся добавить,
// с конструктором документа справа налево. Когда мы добавляем текст с этим флагом, установленным в значение true,
// он будет отформатирован с использованием набора настроек шрифта «справа налево».
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Установите флаг на false, а затем добавьте текст слева направо.
// Конструктор документов отформатирует их, используя набор настроек шрифта слева направо.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
