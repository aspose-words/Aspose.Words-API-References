---
title: DocumentBuilder.MoveToField
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci belgedeki bir alana taşır.
type: docs
weight: 510
url: /tr/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

İmleci belgedeki bir alana taşır.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| field | Field | İmlecin taşınacağı alan. |
| isAfter | Boolean | Doğru olduğunda, imleci alan bitiminden sonra olacak şekilde hareket ettirir. Yanlış olduğunda, imleci alan başlangıcından önce olacak şekilde hareket ettirir. |

### Örnekler

Belge oluşturucunun düğüm ekleme noktası imlecinin belirli bir alana nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder'ı kullanarak bir alan ekleyin ve ondan sonra bir metin dizisi ekleyin.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Oluşturucunun imleci şu anda belgenin sonunda.
Assert.Null(builder.CurrentNode);

// İmleci alandan önce mi sonra mı yerleştireceğinizi belirtirken imleci alana taşıyın.
builder.MoveToField(field, moveCursorToAfterTheField);

// Her iki durumda da imlecin alanın dışında olduğuna dikkat edin.
// Bu, oluşturucuyu bu şekilde kullanarak alanı düzenleyemeyeceğimiz anlamına gelir.
// Bir alanı düzenlemek için, alanın FieldStart'ında oluşturucunun MoveTo yöntemini kullanabiliriz
// veya imleci içine yerleştirmek için FieldSeparator düğümü.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


