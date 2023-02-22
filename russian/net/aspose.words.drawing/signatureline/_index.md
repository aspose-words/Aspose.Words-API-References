---
title: Class SignatureLine
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.SignatureLine сорт. Предоставляет доступ к свойствам строки подписи.
type: docs
weight: 1150
url: /ru/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Предоставляет доступ к свойствам строки подписи.

```csharp
public class SignatureLine
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Получает или задает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписание». Значение по умолчанию для этого свойства: **ЛОЖЬ** . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Получает или задает значение, указывающее, что инструкции по умолчанию отображаются в диалоговом окне Sign. Значение по умолчанию для этого свойства: **истинный** . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Получает или задает предполагаемый адрес электронной почты подписывающей стороны. Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Получает или устанавливает идентификатор для этой строки подписи. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Получает или задает инструкции для подписывающей стороны, которые отображаются при подписании строки подписи. Это свойство игнорируется, если[`DefaultInstructions`](./defaultinstructions/) установлено. Значение по умолчанию для этого свойства **пустой строки** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Указывает, что строка подписи подписана цифровой подписью. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Указывает, что строка подписи подписана цифровой подписью и эта цифровая подпись действительна. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Получает или задает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию: "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Получает или задает значение, указывающее, что дата подписания отображается в строке подписи. Значение по умолчанию для этого свойства: **истинный** . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Получает или задает предполагаемую подписывающую сторону строки подписи. Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Получает или задает предлагаемый титул подписавшего (например, Менеджер). Значение по умолчанию для этого свойства: **пустой строки** (Empty ). |

### Примеры

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

// Вставляем фигуру, которая будет содержать строку подписи, внешний вид которой мы будем
// настроить с помощью объекта «SignatureLineOptions», который мы создали выше.
// Если мы вставим фигуру, координаты которой начинаются в правом нижнем углу страницы,
// нам нужно указать отрицательные координаты x и y, чтобы отобразить фигуру.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Проверяем свойства нашей строки подписи через ее объект Shape.
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


