---
title: DocumentBuilder.InsertSignatureLine
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет строку подписи в текущую позицию.
type: docs
weight: 450
url: /ru/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Вставляет строку подписи в текущую позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, хранящий параметры создания строки подписи. |

### Возвращаемое значение

Узел строки подписи, который был только что вставлен.

### Примеры

Показывает, как подписать документ личным удостоверением и строкой подписи.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Снова открываем сохраненный документ и проверяем, что свойства «IsSigned» и «IsValid» равны «true»,
// указываем, что строка подписи содержит подпись.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Вставляет строку подписи в указанную позицию.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Объект, хранящий параметры создания строки подписи. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до линии подписи. |
| left | Double | Расстояние в пунктах от начала координат до левой части линии подписи. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до линии подписи. |
| top | Double | Расстояние в пунктах от начала координат до верхней части линии подписи. |
| wrapType | WrapType | Указывает, как обтекать строку подписи текстом. |

### Возвращаемое значение

Узел строки подписи, который был только что вставлен.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить в документ встроенную строку подписи.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// Строку подписи можно подписать в Microsoft Word, дважды щелкнув ее.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


