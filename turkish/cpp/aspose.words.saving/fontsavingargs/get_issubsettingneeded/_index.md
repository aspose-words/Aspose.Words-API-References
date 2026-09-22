---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded yöntemi"
linktitle: "get_IsSubsettingNeeded"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded yöntemi. Geçerli yazı tipinin, C++'ta bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt küme oluşturulup oluşturulmayacağını belirtmenizi sağlar."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Geçerli yazı tipinin bir yazı tipi kaynağı olarak dışa aktarılmadan önce alt küme oluşturulup oluşturulmayacağını belirtmeye olanak tanır.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Açıklamalar


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

Varsayılan olarak, Aspose.Words, orijinal yazı tipi dosya boyutunu [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/) içinde belirtilenle karşılaştırarak alt küme oluşturulup oluşturulmayacağına karar verir. Bireysel yazı tipleri için bu davranışı, [IsSubsettingNeeded](./) özelliğini ayarlayarak geçersiz kılabilirsiniz.
## Ayrıca Bakınız

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
