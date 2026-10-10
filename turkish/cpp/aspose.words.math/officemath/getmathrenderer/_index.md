---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer yöntemi"
linktitle: "GetMathRenderer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer yöntemi. C++'ta bu denklemi bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


Bu denklemi bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

Bu denklem için renderleyici nesnesi.
## Açıklamalar


Bu yöntem sadece [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) yapıcısını çağırır ve bu nesneyi parametre olarak geçirir.

## Örnekler



Yerel dosya sisteminde bir Office [Math](../../) nesnesini görüntü dosyasına nasıl renderleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// \"ImageSaveOptions\" nesnesi oluşturun ve düğüm renderleyicisinin \"Save\" yöntemine geçerek değiştirmek için
// OfficeMath düğümünün bir görüntüye nasıl renderlendiğini.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// \"Scale\" özelliğini 5 olarak ayarlayın, nesneyi orijinal boyutunun beş katına renderlemek için.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Ayrıca Bakınız

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
