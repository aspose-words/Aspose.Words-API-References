---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words for .NET
description: DocumentBuilder MoveToField yöntem. İmleci belgedeki bir alana taşır C#'da.
type: docs
weight: 530
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
| isAfter | Boolean | Ne zaman`doğru` , imleci alanın sonundan sonraya taşır. Ne zaman`YANLIŞ`, imleci alan başlangıcından önce olacak şekilde hareket ettirir. |

## Örnekler

Belge oluşturucunun düğüm ekleme noktası imlecinin belirli bir alana nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder'ı kullanarak bir alan ekleyin ve ardından bir metin dizisi ekleyin.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Oluşturucunun imleci şu anda belgenin sonundadır.
Assert.Null(builder.CurrentNode);

// İmlecin alanın önüne mi yoksa arkasına mı yerleştirileceğini belirlerken imleci alana taşıyın.
builder.MoveToField(field, moveCursorToAfterTheField);

// Her iki durumda da imlecin alanın dışında olduğuna dikkat edin.
// Bu, oluşturucuyu bu şekilde kullanarak alanı düzenleyemeyeceğimiz anlamına gelir.
// Bir alanı düzenlemek için, alanın FieldStart'ında oluşturucunun MoveTo yöntemini kullanabiliriz
// veya İmleci içeriye yerleştirmek için FieldSeparator düğümü.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
