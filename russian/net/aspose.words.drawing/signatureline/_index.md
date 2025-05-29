---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.SignatureLine, который позволяет легко управлять свойствами строки подписи и настраивать их для повышения безопасности документа.
type: docs
weight: 1700
url: /ru/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Предоставляет доступ к свойствам строки подписи.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public class SignatureLine
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Возвращает или задает значение, указывающее, может ли подписывающая сторона добавлять комментарии в диалоговом окне «Подписание». Значение по умолчанию для этого свойства —`ЛОЖЬ` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Возвращает или задает значение, указывающее, что в диалоговом окне «Подписать» отображаются инструкции по умолчанию. Значение по умолчанию для этого свойства:`истинный` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Возвращает или задает адрес электронной почты предполагаемого подписчика. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Получает или задает идентификатор для этой строки подписи. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Возвращает или задает инструкции для подписывающего, которые отображаются при подписании строки подписи. Это свойство игнорируется, если[`DefaultInstructions`](./defaultinstructions/) установлено. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Указывает, что строка подписи подписана цифровой подписью. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Указывает, что строка подписи подписана цифровой подписью и эта цифровая подпись действительна. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Возвращает или задает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию: "{00000000-0000-0000-0000-0000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Возвращает или задает значение, указывающее, отображается ли дата подписи в строке подписи. Значение по умолчанию для этого свойства:`истинный` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Возвращает или задает предлагаемого подписчика строки подписи. Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Возвращает или задает предлагаемую должность подписчика (например, Менеджер). Значение по умолчанию для этого свойства:**пустая строка** (Empty ). |

## Примеры

Показывает, как создать строку для подписи и вставить ее в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Вставляем фигуру, которая будет содержать строку подписи, внешний вид которой мы
// настраиваем с помощью объекта «SignatureLineOptions», который мы создали выше.
// Если мы вставим фигуру, координаты которой начинаются в правом нижнем углу страницы,
// нам нужно будет указать отрицательные координаты x и y, чтобы сделать фигуру видимой.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Проверяем свойства нашей линии подписи с помощью ее объекта Shape.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
